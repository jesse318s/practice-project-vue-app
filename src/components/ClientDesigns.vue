<template>
  <TestDesignSection />

  <h3>Entangle - Sass Animation</h3>
  <DesignSection1 style="margin-top: 130px" />
</template>

<script>
import TestDesignSection from "./TestDesignSection.vue";
import DesignSection1 from "./DesignSection1.vue";

export default {
  name: "ClientDesigns",
  props: {
    testingProps: String,
  },
  components: {
    TestDesignSection,
    DesignSection1,
  },
};
</script>
