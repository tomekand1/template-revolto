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
            <h3 class="title iq-tw-7">Compare Services</h3>
          </div>
        </div>
      </div>

      <div class="col-sm-5">
        <div class="iq-services-box text-left iq-font-white">
          <div class="iq-icon">
            <i aria-hidden="true" class="ion-ios-color-wand-outline" />
          </div>
          <div class="services-content">
            <h5 class="iq-tw-6 iq-pb-10 iq-font-white">Unique Design</h5>
            <p>Sofbox’s harmonious design and super clean looks will make your website look beautiful and elegant. It makes your creation look good.</p>
            <div class="iq-progress-bar">
              <p class="iq-progress-bar-text">
                <span>40</span>
              </p>
              <div class="iq-progress-bar">
                <span data-percent="40" />
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
