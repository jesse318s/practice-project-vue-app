<template>
  <div class="special_effect_container">
    <div className="special_effect"></div>
  </div>
</template>

<script>
export default {
  name: "DesignSection2",
};
</script>

<style scoped lang="scss">
.special_effect_container {
  height: 0;
  overflow: visible;
}

.special_effect {
  // new content goes here
}

// sample content to delete
.special_effect::after {
  content: "Design Content";
  position: relative;
  bottom: 16px;
}
</style>
