<template>
  <div class="leaflet-map">
    <div id="map" class="map"></div>
  </div>
</template>

<script>
  import L from 'leaflet';

  export default {
    name: 'leaflet-map',
    data() {
      return {
        center: [48.868, 2.333],
        zoom: 13,
      };
    },
    mounted() {
      const map = L.map('map', this.$data);
      L.tileLayer('https://api.mapbox.com/styles/v1/mapbox/streets-v10/tiles/256/{z}/{x}/{y}?access_token={accessToken}', {
        attribution: 'Map data &copy; <a href="http://openstreetmap.org">OpenStreetMap</a> contributors, <a href="http://creativecommons.org/licenses/by-sa/2.0/">CC-BY-SA</a>, Imagery © <a href="http://mapbox.com">Mapbox</a>',
        maxZoom: 18,
        accessToken: 'pk.eyJ1IjoiamJ1Z2V0IiwiYSI6ImNpeG1pdXIxdjAxdXEyeHBoYjA4c25rengifQ.h8XHihbWbP1rGv7GzZypdA',
      }).addTo(map);
    },
  };
</script>

<style scoped>

  @import '../../node_modules/leaflet/dist/leaflet.css';

  #map {
    position: absolute;
    top: 0;
    bottom: 0;
    width: 100%;
  }

</style>
