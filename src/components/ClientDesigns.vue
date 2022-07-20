<!-- main component for design sections -->
<template>
  <header>
    <h1>Client Designs</h1>
  </header>

  <main>
    <div class="section_divider"></div>

    <h3>Test Section</h3>
    <TestDesignSection />

    <div class="section_divider"></div>

    <h3>Example Section</h3>
    <DesignSection1 style="margin-top: 130px" />

    <div class="section_divider"></div>

    <h3>New Section</h3>
    <DesignSection2 style="margin-top: 130px" />

    <div class="section_divider"></div>

    <h3>Section 3</h3>
    <DesignSection3 style="margin-top: 130px" />

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
import DesignSection3 from "./DesignSection3.vue";

export default {
  name: "ClientDesigns",
  props: {
    testMsg: String,
  },
  components: {
    TestDesignSection,
    DesignSection1,
    DesignSection2,
    DesignSection3,
  },
};
</script>

<style scoped>
.section_divider {
  border-top: 2px solid;
  margin: 2px;
}
</style>
