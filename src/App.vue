<template>
  <ClientDesigns
    testingProps="this prop value is the testing image's alt value"
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
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
.testingSectionStyle {
  content: "Testing Section";
  border-style: solid;
  border-width: 2px;
}
.testingSectionStyle::before {
  content: "Testing Section";
}
</style>
