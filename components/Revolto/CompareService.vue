<template>
  <ParallaxStyle1
    ids="compare-services"
    :bg-image="require('../../assets/images/bg/05.png')"
    class-names="iq-compare-services overview-block-ptb iq-over iq-over-blue-90 iq-parallax"
  >
    <div class="container">
      <div class="row">
        <div class="col-sm-12">
          <div class="heading-title white">
            <h3 class="title iq-tw-7">O nas</h3>
          </div>
        </div>
      </div>
      <div class="row">
        <div class="col-sm-5">
          <div class="iq-services-box text-left iq-font-white">
            <div class="iq-icon">
              <i aria-hidden="true" class="ion-ios-color-wand-outline" />
            </div>
            <div class="services-content">
              <h5
                class="iq-tw-6 iq-pb-10 iq-font-white"
              >Umów się na bezpłatny audyt w dogodnym dla Ciebie terminie!</h5>
              <p>Dobrze dobrana i zamontowana instalacja będzie działała ponad 25 lat! Pracujemy tylko na najlepszych komponentach, współpracujemy z największymi z branży, gwarancje sięgają nawet 25 lat. To gwarancja bezpieczeństwa i tego, że inwestycja się zwróci.</p>
              <div class="iq-progress-bar">
                <p class="iq-progress-bar-text">
                  <span>25</span>
                </p>
                <div class="iq-progress-bar">
                  <span data-percent="98" />
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </ParallaxStyle1>
</template>
<script>
export default {
  name: "CompareService"
};
</script>
