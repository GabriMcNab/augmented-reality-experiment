<template>
  <a-scene embedded arjs vr-mode-ui="enabled: false">
    <a-marker
      type="pattern"
      url="https://raw.githubusercontent.com/GabriMcNab/augmented-reality-experiment/master/src/assets/marker/tui.patt"
    >
      <a-entity rotation="-90 0 0" position="0 0 -3">
        <a-entity position="1.2 0 0">
          <maps-button></maps-button>
        </a-entity>
        <a-entity position="-1.8 0 0">
          <maps-directions :directionsData="directions.car"></maps-directions>
        </a-entity>
        <a-entity position="-1.8 -0.8 0">
          <maps-directions
            :directionsData="directions.walking"
          ></maps-directions>
        </a-entity>
      </a-entity>
    </a-marker>
    <a-entity camera></a-entity>
  </a-scene>
</template>

<script>
import MapsButton from "./components/MapsButton/MapsButton.vue";
import MapsDirections from "./components/MapsDirections/MapsDirections.vue";

export default {
  name: "App",
  components: {
    MapsButton,
    MapsDirections
  },
  data: () => ({
    directions: {
      car: {
        type: "car",
        via: "via Via Aurelia",
        time: "5 min",
        distance: "2.5 Km"
      },
      walking: {
        type: "walking",
        via: "via Via Aurelia",
        time: "26 min",
        distance: "2.1 Km"
      }
    }
  })
};
</script>

<style lang="scss"></style>
