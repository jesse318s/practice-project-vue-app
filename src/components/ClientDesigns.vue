<!-- main component for displaying designs via section components -->
<template>
  <header>
    <h1>Client Designs</h1>
  </header>

  <main>
    <h3>Test Design Section</h3>
    <TestDesignSection />
    <div class="section_divider"></div>

    <h3>Example Design Section</h3>
    <ExampleDesignSection />
    <div class="section_divider"></div>

    <h3>Design Section 1</h3>
    <DesignSection1 />
    <div class="section_divider"></div>
  </main>

  <footer>
    <p>&copy; 2022 Jesse Sites All Rights Reserved.</p>
  </footer>
</template>

<script>
import TestDesignSection from "./TestDesignSection.vue";
import ExampleDesignSection from "./ExampleDesignSection.vue";
import DesignSection1 from "./DesignSection1.vue";

export default {
  name: "ClientDesigns",
  props: {
    testMsg: String,
  },
  components: {
    TestDesignSection,
    ExampleDesignSection,
    DesignSection1,
  },
};
</script>

<style scoped>
header,
main,
footer {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

.section_divider {
  border-top: 2px solid;
  margin: 2px;
}
</style>
