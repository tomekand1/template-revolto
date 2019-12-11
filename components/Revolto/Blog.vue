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
        <div class="row">
          <div class="col-sm-12">
            <div
              class="owl-carousel"
              data-nav="true"
              data-dots="false"
              data-items="3"
              data-items-laptop="3"
              data-items-tab="2"
              data-items-mobile="2"
              data-items-mobile-sm="1"
              data-margin="30"
            >
              <div
                class="item"
                @click="openBmodal(blog)"
                v-for="(blog,index) in blogData"
                :key="index"
              >
                <CardStyle1>
                  <div slot="cardMedia">
                    <div class="img-25">
                      <img :src="blog.link_to_picture" alt="#" />
                    </div>
                  </div>
                  <div slot="cardTitle">
                    <h5 class="iq-tw-7 iq-mb-10">{{blog.title}}</h5>
                  </div>
                  <div slot="cardBody">
                    <p>{{blog.description.slice(0,25)+"..."}}</p>
                  </div>
                  <div slot="cardFooter">
                    <ul class="list-inline">
                      <li class="list-inline-item">
                        <a href="javascript:void(0)">
                          <i class="fa fa-calendar" aria-hidden="true" /> 12 Aug 2019
                        </a>
                      </li>
                    </ul>
                  </div>
                </CardStyle1>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>
<script>
export default {
  name: "Blog",
  data() {
    return {
      blogData: [
        {
          image_id: 1,
          title: "API Reference",
          description:
            "If you are looking for information on a specific function, class, or method, this part of the documentation is for you.",
          link_to_picture: `https://picsum.photos/800/600`
        },
        {
          image_id: 2,
          title: "Miscellaneous Pages",
          description: "descrip",
          link_to_picture: `https://picsum.photos/800/601`
        },
        {
          image_id: 3,
          title: "Miscellaneous",
          description: "descr",
          link_to_picture: `https://picsum.photos/800/602`
        },
        {
          image_id: 4,
          title: "Pages",
          description:
            " It’s highly configurable but comes with sensible defaults out of the box.",
          link_to_picture: `https://picsum.photos/800/604`
        },
        {
          image_id: 1,
          title: "API Reference",
          description:
            "If you are looking for information on a specific function, class, or method, this part of the documentation is for you.",
          link_to_picture: `https://picsum.photos/800/600`
        },
        {
          image_id: 2,
          title: "Miscellaneous Pages",
          description: "descrip",
          link_to_picture: `https://picsum.photos/800/601`
        },
        {
          image_id: 3,
          title: "Miscellaneous",
          description: "descr",
          link_to_picture: `https://picsum.photos/800/602`
        },
        {
          image_id: 4,
          title: "Pages",
          description:
            " It’s highly configurable but comes with sensible defaults out of the box.",
          link_to_picture: `https://picsum.photos/800/604`
        }
      ]
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
          footerClass: "p-2 border-top-0"
        });
      }
    }
  }
};
</script>

<style>
[class^="img"] {
  display: inline-block;
  /*
        Uncomment to see div dimensions
    
        border: 1px dotted red;
    */
}

[class^="img"] img {
  display: block;
}

.img-25 img {
  max-width: 100%;
}
</style>