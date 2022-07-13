<template>
  <div class="special_effect_container">
    <div class="special_effect"></div>
  </div>
</template>

<script>
export default {
  name: "DesignSection1",
};
</script>

<style scoped lang="scss">
.special_effect_container {
  height: 0;
  overflow: visible;
}
.special_effect {
  position: relative;
  bottom: 75px;
  left: 170px;
  transform: rotateX(-20deg) rotateY(20deg) translateX(200px) scaleX(2)
    scaleY(0.89);
  animation: quantumEntangle 750ms infinite linear;
  border-radius: 25px;
  width: 10px;
  height: 10px;
  background: linear-gradient(
    to top,
    rgb(47, 0, 255) 0%,
    rgb(0, 153, 255) 33%,
    rgba(255, 255, 255, 1) 100%
  );
  box-shadow: 1px 1px blue;

  @keyframes quantumEntangle {
    25% {
      transform: rotateY(180deg);
    }
    50% {
      transform: rotateX(360deg) rotateY(-180deg) translateX(-20px) scaleX(1);
    }
    75% {
      transform: rotateY(180deg);
    }
    100% {
      transform: rotateX(360deg) rotateY(180deg) translateX(-20px) scaleX(1);
    }
  }
}
</style>
