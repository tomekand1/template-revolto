<template>
  <ParallaxStyle1
    class-names="iq-ptb-100 iq-counter-box iq-bg-over iq-over-blue-90 iq-font-white iq-parallax"
    :bg-image="image"
    ids="counter"
  >
    <div class="container">
      <div>
        <div class="heading-title white">
          <h3 class="title iq-tw-7">{{this.$store.state.dataToPull.settings.offer.title}}</h3>
        </div>
      </div>

      <div class="counter-info iq-mt-60 iq-pt-60">
        <div class="row">
          <div class="col-lg-6">
            <p class="iq-mt-30">{{this.$store.state.dataToPull.settings.offer.description1}}</p>
          </div>
          <div class="col-lg-6">
            <div class="counter-info-img">
              <img class="center-block" :src="require('../../assets/images/drive/07.png')" alt="#" />
            </div>
          </div>
        </div>
      </div>
    </div>

    <div class="container">
      <div>
        <div class="heading-title white"></div>
      </div>

      <div class="counter-info iq-mt-60 iq-pt-60">
        <div class="row">
          <div class="col-lg-6">
            <p class="iq-mt-30">{{this.$store.state.dataToPull.settings.offer.description2}}</p>
          </div>
          <div class="col-lg-6">
            <div class="counter-info-img">
              <img
                class="center-block"
                :src="require('../../assets/images/drive/ceny-pradu.png')"
                alt="#"
              />
            </div>
          </div>
        </div>
      </div>
    </div>

    <div class="container">
      <div>
        <div class="heading-title white"></div>
      </div>

      <div class="counter-info iq-mt-60 iq-pt-60">
        <div class="row">
          <div class="col-lg-6">
            <p class="iq-mt-30">{{this.$store.state.dataToPull.settings.offer.description3}}</p>
          </div>
          <div class="col-lg-6">
            <div class="counter-info-img">
              <img
                class="center-block"
                :src="require('../../assets/images/drive/Schemat.png')"
                alt="#"
              />
            </div>
          </div>
        </div>
      </div>
    </div>
  </ParallaxStyle1>
</template>
<script>
import countTo from "vue-count-to";
export default {
  name: "Counter",
  components: {
    countTo
  },
  data() {
    return {
      image: require("../../assets/images/bg/02.png")
    };
  }
};
</script>
