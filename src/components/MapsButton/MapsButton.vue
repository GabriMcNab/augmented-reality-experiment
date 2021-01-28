<template>
  <a-entity emitevents="true" cursor="rayOrigin: mouse" @click="openGoogleMaps">
    <a-image :src="button" height="0.3" id="MapsButton"></a-image>
  </a-entity>
</template>

<script>
import button from "../../assets/img/button.png";

const MAPS_BASE_URL = "https://www.google.com/maps/search/";

export default {
  name: "MapsButton",
  data() {
    return {
      button
    };
  },
  methods: {
    openGoogleMaps() {
      const url = `${MAPS_BASE_URL}?api=1&query=Via+Vespasiano,468+00192+Roma+RM`;
      window.open(url, "_blank");
    }
  }
};
</script>

<style></style>
