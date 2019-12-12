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
            <div class="item">
              <CardStyle7>
                <div slot="cardMedia"></div>
                <div slot="cardHeader">
                  <h5 class="iq-tw-6">Natalia Z.</h5>
                </div>
                <div slot="cardBody">
                  <p>Wielki pozytyw. Pełen profesjonalizm i zaangażowanie w sprawie. Szybko i sprawnie zajęto się moja sprawą, materiały dowodowe sprawiły że uzyskałam jasna odpowiedź na zlecaną sprawę. Tomasz w trudnych dla mnie chwilach wykazał się duża cierpliwością i empatią oraz wsparciem.</p>
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
export default {
  name: "Testimonial"
};
</script>
