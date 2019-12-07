<template>
  <section id="questions" class="overview-block-ptb white-bg iq-asked">
    <div class="container">
      <div class="row">
        <div class="col-sm-12">
          <div class="heading-title">
            <h3 class="title iq-tw-7">Pytania</h3>
            <p>Najczesciej zadawane pytania.</p>
          </div>
        </div>
      </div>

      <div class="row align-items-center">
        <div class="col-md-12 col-lg-6">
          <img
            class="img-fluid center-block"
            :src="require('../../assets/images/drive/10.png')"
            alt="drive10"
            style="z-index: 9; position: relative;"
          />
        </div>

        <div class="col-md-12 col-lg-6">
          <div class="iq-accordion">
            <div class="iq-accordion">
              <a
                href="javascript:void(0)"
                class="accordion-title iq-tw-7 iq-font-grey"
              >Kliknij na pytanie...</a>
              <div class="accordion-details">
                <div class="row">
                  <div class="col-sm-9">Aby zobaczyć odpowiedź...</div>
                </div>
              </div>
            </div>

            <div class="iq-accordion" v-for="question in questions">
              <a
                href="javascript:void(0)"
                class="accordion-title iq-tw-7 iq-font-grey"
              >{{question.title}}</a>
              <div class="accordion-details">{{question.answer}}</div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="iq-objects-asked">
      <span class="iq-objects-01">
        <img :src="require('../../assets/images/drive/02.png')" alt="drive02" />
      </span>
      <span
        class="iq-objects-02"
        data-bottom="transform:translatex(50px)"
        data-top="transform:translatex(-100px);"
      >
        <img :src="require('../../assets/images/drive/04.png')" alt="drive02" />
      </span>
      <span class="iq-objects-03 iq-fadebounce">
        <span class="iq-round" />
      </span>
    </div>
  </section>
</template>
<script>
export default {
  name: "Faq",
  data() {
    return {
      questions: this.$store.state.questionsData.questions
    };
  }
};
</script>
