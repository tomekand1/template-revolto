<template>
  <div>
    <Home />
    <div class="main-content">
      <HomeDescription />
      <Offer />
      <Finance />

      <CompareService />
      <Faq />
      <Blog />
      <Client />
      <Testimonial />
      <footer>
        <ParallaxStyle1
          :bg-image="require('../../assets/images/bg/09.jpg')"
          ids="iq-home"
          class-names="iq-ptb-100 iq-newsletter iq-bg-over iq-over-blue-90 jarallax"
        >
          <div class="container">
            <div class="row">
              <div class="col-sm-12">
                <div class="heading-title white iq-mb-25">
                  <h3 class="title iq-tw-7">Kontakt</h3>
                </div>
              </div>
            </div>
            <div class="row justify-content-center">
              <div class="col-lg-7"></div>
            </div>
          </div>
        </ParallaxStyle1>
        <Contact />
        <FooterStyle3>
          <p slot="address">{{this.$store.state.dataToPull.kontakt.address}}</p>
          <p slot="phone">
            {{this.$store.state.dataToPull.kontakt.phone}}
            <br />
            {{this.$store.state.dataToPull.kontakt.godzinyOtwarcia}}
            <br />
          </p>
          <p slot="mail">
            {{this.$store.state.dataToPull.kontakt.mail}}
            <br />
          </p>
          <ul slot="links">
            <li v-if="this.$store.state.dataToPull.kontakt.twitter">
              <a :href="this.$store.state.dataToPull.kontakt.twitter">
                <i class="fab fa-twitter" />
              </a>
            </li>
            <li v-if="this.$store.state.dataToPull.kontakt.facebook">
              <a :href="this.$store.state.dataToPull.kontakt.facebook">
                <i class="fab fa-facebook" />
              </a>
            </li>

            <li v-if="this.$store.state.dataToPull.kontakt.instagram">
              <a :href="this.$store.state.dataToPull.kontakt.instagram">
                <i class="fab fa-instagram" />
              </a>
            </li>
          </ul>
        </FooterStyle3>
      </footer>
    </div>
    <ColorCustomizer />
    <ScrollTop />
  </div>
</template>

<script>
import Home from "../../components/Revolto/Home";
import Finance from "../../components/Revolto/Finance";
import HomeDescription from "../../components/Revolto/HomeDescription";
import Offer from "../../components/Revolto/Offer";
import Testimonial from "../../components/Revolto/Testimonial";

import CompareService from "../../components/Revolto/CompareService";
import Faq from "../../components/Revolto/Faq";
import Blog from "../../components/Revolto/Blog";
import Client from "../../components/Revolto/Client";
import Contact from "../../components/Revolto/Contact";
import { sofbox } from "../../assets/app/app";

export default {
  layout: "Revolto",
  components: {
    Home,
    Finance,
    HomeDescription,
    Offer,
    Testimonial,
    CompareService,
    Faq,
    Blog,
    Client,
    Contact
  },
  mounted() {
    setTimeout(function() {
      sofbox.index();
      //  sofbox.magnific();
    }, 1000);
  }
};
</script>
