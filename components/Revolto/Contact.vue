<template>
  <section id="contact-us" class="footer-info white-bg">
    <div class="container">
      <div class="row justify-content-end">
        <div class="col-md-6 col-lg-4">
          <div class="iq-get-in">
            <h4 class="iq-tw-7 iq-mb-20">Skontaktuj się z nami</h4>
            <ContactForm />
          </div>
        </div>
      </div>
    </div>
    <iframe
      class="map"
      src="https://www.google.pl/maps/embed?pb=!1m18!1m12!1m3!1d2439.384050509195!2d16.40608131586519!3d52.30903325959456!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x470433b802667f49%3A0x4bc79d245ef60c56!2sPowsta%C5%84ca%20Kozaka%2013%2C%2064-330%20Opalenica%2C%20Poland!5e0!3m2!1sen!2suk!4v1576071948095!5m2!1sen!2suk"
      style="border:0;"
      allowfullscreen
    ></iframe>
  </section>
</template>
<script>
export default {
  name: "Contact"
};
</script>
