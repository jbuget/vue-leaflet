<template>
  <div id="app">
    <leaflet-map></leaflet-map>
  </div>
</template>

<script>
import LeafletMap from './components/LeafletMap';

export default {
  name: 'app',
  components: {
    LeafletMap,
  },
};
</script>

<style>

  body { margin:0; padding:0; }

</style>
