<!-- new design section -->
<template>
  <div class="special_effect_container">
    <div class="special_effect" ref="specialEffect">
      <div class="special_effect_sample" ref="specialEffectSample"></div>
    </div>
  </div>
</template>

<script>
export default {
  name: "DesignSection2",
  methods: {
    // function that checks if the "special_effect" SCSS class is being used correctly, hides sample content if so, and displays a console message if not
    effectUseCheck() {
      // select special effect element by Vue reference
      const effectElement = this.$refs.specialEffect;

      // get the SCSS for the effect element
      const effectStyles = window.getComputedStyle(effectElement);

      // access the position property of the retrieved style
      const effectPositon = effectStyles.position;

      // check if the positon property is relative, and hide sample content if so
      if (effectPositon === "relative") {
        // select special effect sample element by Vue reference
        const effectSampleElement = this.$refs.specialEffectSample;

        // get the SCSS for the effect sample element
        const effectSampleStyle = effectSampleElement.style;

        // set the display property of the retrieved style to none
        effectSampleStyle.display = "none";
      } else {
        // displays a console message if the special effect is not being used correctly
        console.log(
          'Please add the "position: relative;" property value to the "special_effect" class in order hide the sample content.'
        );
      }
    },
  },
  mounted: function () {
    // special effect correct usage is checked after component is mounted
    this.effectUseCheck();
  },
};
</script>

<style scoped lang="scss">
.special_effect_container {
  height: 0;
  overflow: visible;
}

/* new SCSS content goes in this "special_effect" class -
using the "position: relative;" property value in this class will hide this section's sample content */
.special_effect {
  position: static;
}

// sample content which is not visible when the "special_effect" class has the "position: relative;" property value
.special_effect_sample::after {
  content: "Design Content";
  position: relative;
  bottom: 16px;
}
</style>
