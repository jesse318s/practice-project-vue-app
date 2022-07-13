<template>
  <div class="testingSectionStyle">
    <img
      src="../assets/testingImg.png"
      v-bind:alt="testingProps"
      width="300"
      height="300"
    />
  </div>
</template>

<script>
export default {
  name: "TestDesignSection",
};
</script>

<style scoped lang="scss">
.testingSectionStyle::after {
  content: "Scss is active.";
}
</style>
