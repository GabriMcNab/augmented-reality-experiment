<template>
  <a-scene embedded arjs>
    <a-marker
      type="pattern"
      url="https://raw.githubusercontent.com/GabriMcNab/augmented-reality-experiment/master/src/assets/marker/tui.patt"
    >
      <a-entity rotation="-90 0 0" position="0 0 -3">
        <a-entity position="1.2 0 0">
          <maps-button></maps-button>
        </a-entity>
      </a-entity>
    </a-marker>
    <a-entity camera></a-entity>
  </a-scene>
</template>

<script>
import MapsButton from "./components/MapsButton/MapsButton.vue";

export default {
  name: "App",
  components: {
    MapsButton
  }
};
</script>

<style lang="scss"></style>
