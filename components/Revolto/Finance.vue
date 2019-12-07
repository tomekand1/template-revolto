<template>
  <div>
    <section id="how-it-works" class="overview-block-ptb it-works">
      <div class="container">
        <div class="row">
          <div class="col-sm-12">
            <div class="heading-title">
              <h3 class="title iq-tw-7">
                {{ this.$store.state.dataToPull.about.title
                }}
              </h3>
              <p>
                {{ this.$store.state.dataToPull.about.description
                }}
              </p>
            </div>
          </div>
        </div>
      </div>
    </section>
    <SectionStyle1>
      <div slot="cardBody" class="col-lg-6">
        <div class="heading-title left text-left">
          <h3 class="iq-tw-7 iq-mb-25 title">
            {{ this.$store.state.dataToPull.dotacja.title
            }}
          </h3>
        </div>
        <p>
          {{ this.$store.state.dataToPull.dotacja.description1
          }}
        </p>
        <p class="iq-mt-20">
          {{ this.$store.state.dataToPull.dotacja.description2
          }}
        </p>
        <h6 class="iq-tw-6 iq-mb-15 iq-mt-25">
          {{ this.$store.state.dataToPull.dotacja.boldSign
          }}
        </h6>
      </div>
      <div slot="cardMedia" class="col-lg-6 align-self-center">
        <img
          class="iq-works-img pull-right img-fluid"
          src="../../assets/images/drive/01.png"
          alt="drive01"
        />
      </div>
    </SectionStyle1>
    <SectionStyle2 id :small="small">
      <div slot="cardMedia" class="iq-software-demo">
        <img
          class="img-fluid"
          src="../../assets/images/drive/05.png"
          height="800"
          width="850"
          alt="drive05"
        />
      </div>
      <div slot="cardBody" class="col-lg-6 offset-lg-6">
        <div class="heading-title left text-left">
          <h3 class="iq-tw-7 iq-mb-25 title">
            {{ this.$store.state.dataToPull.kredyt.title
            }}
          </h3>
        </div>
        <p>
          {{ this.$store.state.dataToPull.kredyt.description1
          }}
        </p>
        <ul class="iq-mt-40 iq-list">
          <li v-if="this.$store.state.dataToPull.kredyt.description2" class="iq-tw-6 iq-mb-15">
            <i class="ion-android-done-all iq-mr-10 iq-font-blue iq-font-30"></i>
            <span class="iq-font-black">
              {{ this.$store.state.dataToPull.kredyt.description2
              }}
            </span>
          </li>
          <li v-if="this.$store.state.dataToPull.kredyt.description3" class="iq-tw-6 iq-mb-15">
            <i class="ion-android-done-all iq-mr-10 iq-font-blue iq-font-30"></i>
            <span class="iq-font-black">
              {{ this.$store.state.dataToPull.kredyt.description3
              }}
            </span>
          </li>
          <li v-if="this.$store.state.dataToPull.kredyt.description4" class="iq-tw-6 iq-mb-15">
            <i class="ion-android-done-all iq-mr-10 iq-font-blue iq-font-30"></i>
            <span class="iq-font-black">
              {{ this.$store.state.dataToPull.kredyt.description4
              }}
            </span>
          </li>
        </ul>
      </div>
    </SectionStyle2>
    <SectionStyle1>
      <div slot="cardBody" class="col-lg-6">
        <div class="heading-title left text-left">
          <h3 class="iq-tw-7 iq-mb-25 title">
            {{ this.$store.state.dataToPull.gotowka.title
            }}
          </h3>
        </div>
        <p>
          {{ this.$store.state.dataToPull.gotowka.description1
          }}
        </p>
        <p class="iq-mt-20">
          {{ this.$store.state.dataToPull.gotowka.description2
          }}
        </p>
        <h6 class="iq-tw-6 iq-mb-15 iq-mt-25">
          {{ this.$store.state.dataToPull.gotowka.boldSign
          }}
        </h6>
      </div>
      <div slot="cardMedia" class="col-lg-6 align-self-center">
        <img
          class="iq-works-img pull-right img-fluid"
          src="../../assets/images/drive/gotowka.png"
          alt="drive01"
        />
      </div>
    </SectionStyle1>
  </div>
</template>
<script>
export default {
  name: "About",
  data() {
    return {
      small: true
    };
  }
};
</script>
