<template>
  <header>
    <h1>Client Designs</h1>
  </header>

  <main>
    <div class="section_divider"></div>

    <h3>Test Section</h3>
    <TestDesignSection />

    <div class="section_divider"></div>

    <h3>Entangle - Sass Animation (Example)</h3>
    <DesignSection1 style="margin-top: 130px" />

    <div class="section_divider"></div>

    <h3>Design Label</h3>
    <DesignSection2 style="margin-top: 130px" />

    <div class="section_divider"></div>
  </main>

  <footer>
    <p>&copy; 2022 Jesse Sites All Rights Reserved.</p>
  </footer>
</template>

<script>
import TestDesignSection from "./TestDesignSection.vue";
import DesignSection1 from "./DesignSection1.vue";
import DesignSection2 from "./DesignSection2.vue";

export default {
  name: "ClientDesigns",
  props: {
    testMsg: String,
  },
  components: {
    TestDesignSection,
    DesignSection1,
    DesignSection2,
  },
};
</script>

<style scoped>
.section_divider {
  border-top: 2px solid;
  margin: 2px;
}
</style>
