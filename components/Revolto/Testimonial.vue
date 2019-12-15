<template>
  <section class="overview-block-ptb white-bg iq-loved-customers">
    <div class="container">
      <div class="row">
        <div class="col-sm-12">
          <div class="heading-title">
            <h3 class="title iq-tw-7">Opinie</h3>
            <p>Opinie naszych klientów</p>
          </div>
        </div>
      </div>
      <div class="row">
        <div class="col-sm-12">
          <div
            class="owl-carousel"
            data-autoplay="true"
            data-loop="true"
            data-nav="true"
            data-dots="false"
            data-items="4"
            data-items-laptop="5"
            data-items-tab="2"
            data-items-mobile="1"
            data-items-mobile-sm="1"
            data-margin="30"
          >
            <div class="item" v-for="(opinion,index) in opinions" :key="index">
              <CardStyle7>
                <div slot="cardMedia"></div>
                <div slot="cardHeader">
                  <h5 class="iq-tw-6">{{opinion.opinion_title}}</h5>
                </div>
                <div slot="cardBody">
                  <p>{{opinion.opinion_body}}</p>
                </div>
              </CardStyle7>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
<script>
import axios from "axios";
export default {
  name: "Testimonial",
  data() {
    return {
      opinions: []
    };
  },
  methods: {
    getOpinions() {
      axios
        .get(`${process.env.baseUrl}/api/opinions/`, {
          auth: JSON.parse(sessionStorage.getItem("auth"))
        })
        .then(({ data }) => {
          this.opinions = data;
        });
    }
  },
  mounted() {
    this.getOpinions();
  }
};
</script>
