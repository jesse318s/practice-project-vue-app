<!-- new design section -->
<template>
  <div class="special_effect_container" ref="specialEffectContainer">
    <div class="special_effect" ref="specialEffect">
      <div class="special_effect_sample" ref="specialEffectSample"></div>
    </div>
  </div>
</template>

<script>
export default {
  name: "DesignSection1",
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
          'Please add the "position: relative;" property value to the "special_effect" class to hide the sample content.'
        );
      }
    },
    // set the margin top of the special effect container to the bottom position value of the special effect
    setContainerMargin() {
      // select special effect element by Vue reference
      const effectElement = this.$refs.specialEffect;

      // get the SCSS for the effect element
      const effectStyles = window.getComputedStyle(effectElement);

      // access the bottom property of the retrieved style
      const effectBottom = effectStyles.bottom;

      // set the new effect bottom to 110% of it's original value
      const effectBottomNew = parseInt(effectBottom.replace(/\D/g, "")) * 1.1;

      // select special effect container element by Vue reference
      const containerElement = this.$refs.specialEffectContainer;

      // get the SCSS for the container element
      const containerStyle = containerElement.style;

      // set the margin top of the special effect container to the bottom position value of the special effect
      containerStyle.marginTop =
        effectBottomNew.toString() + effectBottom.replace(/[0-9]/g, "");
    },
  },
  mounted: function () {
    // special effect correct usage is checked after component is mounted
    this.effectUseCheck();
    // special effect container margin is set after compontnent is mounted and special effect usage is checked
    this.setContainerMargin();
  },
};
</script>

<style scoped lang="scss">
/* ********************************


new SCSS content goes in this "special_effect" class -
using the "position: relative;" property value in this class will hide this section's sample content -
the container size is adjusted based on the "bottom" property value of this class -
new SCSS content may also be created and used outside of this class within this style module


******************************** */
.special_effect {
  position: static;
}
</style>
