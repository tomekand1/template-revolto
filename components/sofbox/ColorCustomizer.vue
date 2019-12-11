<template>
  <div class="iq-customizer" :class="panel"></div>
</template>
<script>
export default {
  name: "ColorCustomizer",
  data() {
    return {
      panel: "closed"
    };
  },
  methods: {
    styleChange(color) {
      document.documentElement.style.setProperty(
        "--primary-theme-color",
        color.code
      );
      document.documentElement.style.setProperty(
        "--primary-rgb-theme-color",
        color.rgb
      );
      window.$("#logo_img").attr(
        "src"
        // require("assets/images/color-customizer/" + color.image + ".png")
      );
    }
  },
  mounted() {
    this.styleChange(this.$store.state.dataToPull.color);
  }
};
</script>