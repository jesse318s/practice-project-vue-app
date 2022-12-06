<!-- component for testing Vue, HTML, and SCSS -->
<template>
  <div class="test_section" ref="testSection">
    <!-- img alt is a prop value for Vue testing purposes, made accessible by v-bind -->
    <img src="../assets/testImg.png" :alt="testMsg" width="300" height="300" />
  </div>
</template>

<script>
export default {
  name: "TestDesignSection",
  props: {
    // test message prop is passed down from the ClientDesigns component, which recieves the prop from the App component
    testMsg: String,
  },
  methods: {
    // test function that logs a message if the test section SCSS is not active
    sectionTest() {
      // select test section element by Vue reference
      const sectionElement = this.$refs.testSection;

      // get the SCSS that is after the test section element
      const sectionStylesAfter = window.getComputedStyle(
        sectionElement,
        "::after"
      );

      // access the content property of the retrieved style
      const sectionContentAfter = sectionStylesAfter.content;

      // test if the content property is the expected string
      console.assert(
        sectionContentAfter === '"SCSS is active."',
        "SCSS error."
      );
    },
  },
  mounted: function () {
    "use strict";
    // component is tested after it is mounted
    this.sectionTest();
  },
};
</script>

<style scoped lang="scss">
// content is inserted after the img element by selecting after the test section wrapper
.test_section::after {
  content: "SCSS is active.";
}
</style>
