<template>
  <div class="test_section" ref="testSection">
    <img
      src="../assets/testImg.png"
      v-bind:alt="testMsg"
      width="300"
      height="300"
    />
  </div>
</template>

<script>
export default {
  name: "TestDesignSection",
  props: {
    testMsg: String,
  },
  methods: {
    sectionTest() {
      const sectionElement = this.$refs.testSection;
      const sectionStylesAfter = window.getComputedStyle(
        sectionElement,
        "::after"
      );
      const sectionContentAfter = sectionStylesAfter.content;
      console.assert(
        sectionContentAfter === '"Scss is active."',
        "Scss error."
      );
    },
  },
  mounted: function () {
    this.sectionTest();
  },
};
</script>

<style scoped lang="scss">
.test_section::after {
  content: "Scss is active.";
}
</style>
