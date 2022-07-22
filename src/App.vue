<template>
  <ClientDesigns
    testMsg="This prop value should be set as the testing image's alt value."
  />
</template>

<script>
import ClientDesigns from "./components/ClientDesigns.vue";

export default {
  name: "App",
  components: {
    ClientDesigns,
  },
};
</script>

<style>
.special_effect_container {
  height: 0;
  overflow: visible;
}

/* sample content which is not visible when the "special_effect" class has the "position: relative;" property value */
.special_effect_sample::after {
  content: "Design Content";
  position: relative;
  bottom: 16px;
}
</style>
