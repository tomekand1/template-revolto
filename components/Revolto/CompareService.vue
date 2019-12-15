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
            <h3 class="title iq-tw-7">Umów się na bezpłatny audyt w dogodnym dla Ciebie terminie!</h3>
          </div>
        </div>
      </div>

      <div class="col">
        <div class="iq-services-box iq-font-white">
          <div class="iq-icon">
            <i aria-hidden="true" class="ion-ios-sunny" />
          </div>
          <div class="services-content">
            <h5
              class="iq-tw-6 iq-pb-10 iq-font-white"
            >ZAMÓW BEZPŁATNY AUDYT i dowiedz się jak obniżyć rachunki za prąd lub nie płacić ich wcale instalując panele fotowoltaiczne.</h5>
            <p style="font-style: italic">
              Fotowoltaika to proces przetwarzania energii słonecznej na energię elektryczną. Dzięki systemowi fotowoltaicznemu możesz znacznie obniżyć wysokość rachunków za prąd (np. zapłacisz za prąd tylko ok. 100zł za rok).
              Dobrze dobrana i zamontowana instalacja będzie działała ponad 25 lat! Pracujemy tylko na najlepszych komponentach, współpracujemy z największymi z branży, gwarancje sięgają nawet 25 lat. To gwarancja bezpieczeństwa i tego, że inwestycja się zwróci.
            </p>
          </div>
          <div class="iq-progress-bar">
            <!-- <p class="iq-progress-bar-text">
              <span>100%</span>
            </p>-->
            <div class="iq-progress-bar">
              <span data-percent="100" />
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
