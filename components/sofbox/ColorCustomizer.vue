<template>
  <div class="iq-customizer" :class="panel"></div>
</template>
<script>
export default {
  name: "ColorCustomizer",
  data() {
    return {
      panel: "closed",
      colors: [
        { code: "#4ac4f3", rgb: "74, 196, 243" },
        {
          code: "#8c79f7",
          rgb: "140, 121, 247"
        },
        { code: "#3b90fd", rgb: "59, 144, 253" },
        { code: "#f46d4f", rgb: "244, 109, 79" },
        { code: "#01dabb", rgb: "1, 218, 187" },
        {
          code: "#7570ff",
          rgb: "117, 112, 255"
        },
        { code: "#4a2fb4", rgb: "74, 47, 180" },
        { code: "#80c02b", rgb: "128, 192, 43" },
        { code: "#04cae7", rgb: "4, 202, 231" },
        {
          code: "#7fc129",
          rgb: "127, 193, 41"
        },
        { code: "#ff5033", rgb: "255, 80, 51" },
        {
          code: "#f8a4d8",
          rgb: "248, 164, 216"
        },
        {
          code: "#1edae6",
          rgb: "30, 218, 230"
        },
        { code: "#1ad993", rgb: "26, 217, 147" }
      ]
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
    this.styleChange(this.colors[5]);
  }
};
</script>