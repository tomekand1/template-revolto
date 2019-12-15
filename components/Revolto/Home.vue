<template>
  <ParallaxStyle1
    ids="iq-home"
    :bg-image="bgImage"
    class-names="iq-banner overview-block-pt iq-bg-over iq-over-blue-90 iq-parallax"
  >
    <div class="container-fluid">
      <div class="banner-text">
        <div class="row">
          <div class="col-lg-6">
            <h1 class="text-uppercase iq-font-white iq-tw-3">
              {{ this.$store.state.dataToPull.settings.home.title
              }}
            </h1>
            <p class="iq-font-white iq-pt-15 iq-mb-40">
              {{ this.$store.state.dataToPull.settings.home.description
              }}
            </p>
          </div>
          <div class="col-lg-6">
            <img class="banner-img" :src="require('../../assets/images/banner/01.png')" alt />
          </div>
        </div>
      </div>
    </div>
    <div class="banner-objects">
      <!-- <span
        class="banner-objects-01"
        data-bottom="transform:translatey(50px)"
        data-top="transform:translatey(-50px);"
      >
        <img :src="require('../../assets/images/drive/03.png')" alt="drive02" />
      </span>
      <span class="banner-objects-02 iq-fadebounce">
        <span class="iq-round" />
      </span>-->
      <span class="banner-objects-03 iq-fadebounce">
        <span class="iq-round" />
      </span>
    </div>
  </ParallaxStyle1>
</template>
<script>
import axios from "axios";
import { mapActions } from "vuex";
export default {
  name: "Home",
  data() {
    return {
      bgImage: require("../../assets/images/bg/01.jpg")
    };
  },
  methods: {
    // getData() {
    //   axios.get(`${process.env.baseUrl}/api/settings/1`).then(({ data }) => {
    //     this.settings = data.settings;
    //   });
    // }
    ...mapActions({
      getData: "dataToPull/getData"
    })
  },
  mounted() {
    this.getData();
  }
};
</script>

