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
