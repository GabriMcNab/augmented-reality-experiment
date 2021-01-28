<template>
  <a-entity>
    <a-image :src="imageSrc" height="0.5" width="0.5" position="-0.3 0.4 0.1">
    </a-image>
    <a-text
      :value="directionsData.via"
      color="#333"
      width="4"
      position="0 0.5 0.1"
    ></a-text>
    <a-text
      :value="directionsData.time"
      color="#333"
      width="4"
      position="1.5 0.5 0.1"
    ></a-text>
    <a-text
      value="Details"
      color="#092a5e"
      width="3.5"
      position="0 0.3 0.1"
    ></a-text>
    <a-text
      :value="directionsData.distance"
      color="#757575"
      width="4"
      position="1.5 0.3 0.1"
    ></a-text>
  </a-entity>
</template>

<script>
import car from "../..//assets/img/car.png";
import walking from "../../assets/img/walking.png";

export default {
  name: "MapsDirections",
  props: {
    directionsData: {
      type: Object,
      required: true
    }
  },
  computed: {
    imageSrc() {
      return this.directionsData.type === "car" ? car : walking;
    }
  }
};
</script>

<style></style>
