<template>
  <div data-spy="scroll" data-offset="80">
    <Loader />
    <HeaderStyle1 :logo-img="logo" :nav-item-list="navItems" :styled-logo="styleLogo" />
    <nuxt />
  </div>
</template>
<script>
import logoImg from "../assets/images/logo.png";
export default {
  name: "Revolto",
  head() {
    return {
      bodyAttrs: {
        "data-spy": "scroll",
        "data-offset": "80"
      }
    };
  },
  data() {
    return {
      styleLogo: false,
      logo: logoImg,
      navItems: [
        {
          href: "#iq-home",
          title: "FOTOWOLTAIKA"
        },
        { href: "#how-it-works", title: "FINANSOWANIE" },
        { href: "#questions", title: "PYTANIA" },
        // { href: "#great-screenshots", title: "Screenshots" },
        // { href: "#pricing", title: "CENNY" },
        { href: "#blog", title: "AKTUALNOSCI" },
        { href: "#contact-us", title: "KONTAKT" }
      ]
    };
  },
  mounted() {}
};
</script>
<style>
@import url("../assets/css/color/style.css");
.wow {
  visibility: hidden;
}
@keyframes fadeInUp {
  0% {
    opacity: 0;
    -webkit-transform: translate3d(0, 30%, 0);
    -ms-transform: translate3d(0, 30%, 0);
    transform: translate3d(0, 30%, 0);
  }
  100% {
    opacity: 1;
    -webkit-transform: none;
    -ms-transform: none;
    transform: none;
  }
}

.fadeInUp {
  animation-name: fadeInUp;
  animation-timing-function: ease-out;
}
</style>
