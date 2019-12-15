<template>
  <div>
    <section id="blog" class="overview-block-ptb grey-bg iq-blog blog-section">
      <div class="container">
        <div class="row">
          <div class="col-sm-12">
            <div class="heading-title">
              <h3 class="title iq-tw-7">Aktualności</h3>
              <!-- <p>Below are some of the most popular blogging solutions.</p> -->
            </div>
          </div>
        </div>
        <vue-glide v-if="blogData[0]" type="slide" :breakpoints="size" class="glide__arrow">
          >
          <vue-glide-slide v-for="(blog,index) in blogData" :key="index">
            <CardStyle1>
              <div slot="cardMedia">
                <img class="img" @click="openBmodal(blog)" :src="blog.link_to_picture" alt="#" />
              </div>
              <div slot="cardTitle">
                <h5 @click="openBmodal(blog)" class="iq-tw-7 iq-mb-10">{{blog.title}}</h5>
              </div>
              <div slot="cardBody">
                <p @click="openBmodal(blog)">{{blog.description.slice(0,25)+"..."}}</p>
              </div>
              <div slot="cardFooter">
                <ul class="list-inline">
                  <li class="list-inline-item">
                    <i class="fa fa-calendar" aria-hidden="true" />
                    12 Aug 2019
                  </li>
                </ul>
              </div>
            </CardStyle1>
          </vue-glide-slide>
          <template slot="control">
            <button data-glide-dir="<" class="pos marg button btn ion-chevron-left"></button>
            <button data-glide-dir=">" class="button marg btn ion-chevron-right"></button>
          </template>
        </vue-glide>
      </div>
    </section>
  </div>
</template>
<script>
import { Glide, GlideSlide } from "vue-glide-js";
import "vue-glide-js/dist/vue-glide.css";
import axios from "axios";
export default {
  name: "Blog",
  components: {
    [Glide.name]: Glide,
    [GlideSlide.name]: GlideSlide
  },
  data() {
    return {
      autoplay: 3000,
      size: {
        800: {
          perView: 1
        }
      },
      blogData: []
    };
  },
  methods: {
    openBmodal(blog) {
      {
        const h = this.$createElement;
        // Using HTML string
        // More complex structure
        const messageVNode = h("div", { class: ["foobar"] }, [
          h("b-img", {
            props: {
              src: blog.link_to_picture,
              center: true,
              fluid: true
            }
          }),
          h("p", { class: ["text-center"] }),
          h("h4", { class: ["text-center"] }, [h("strong", {}, blog.title)]),
          h("p", { class: ["text-center"] }),
          h("p", { class: ["text-center"] }, [h("p", {}, blog.description)])
        ]);
        // We must pass the generated VNodes as arrays
        this.$bvModal.msgBoxOk([messageVNode], {
          centered: true,
          size: "lg",
          buttonSize: "sm",
          okVariant: "secondary",
          footerClass: "p-2 border-top-0"
        });
      }
    },
    getImages() {
      axios.get(`${process.env.baseUrl}/api/images`).then(({ data }) => {
        this.blogData = data;
      });
    }
  },
  mounted() {
    this.getImages();
  }
};
</script>

<style>
.img {
  position: relative;
  float: left;

  height: 250px;
  background-position: 50% 50%;
  background-repeat: no-repeat;
  background-size: cover;
}
.marg {
  margin-top: 2em;
}
.pos {
  margin-left: 40%;
  margin-left: 45%;
  margin-right: auto;
}
@media only screen and (max-width: 600px) {
  .pos {
    margin-left: 25%;
    margin-right: auto;
  }
}
</style>