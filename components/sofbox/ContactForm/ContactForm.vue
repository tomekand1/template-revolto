<template>
  <form method="post" @submit.prevent="onSubmit($event)" autocomplete="off">
    <div class="contact-form">
      <div class="section-field">
        <input
          id="contact_name"
          v-model="mailData.name"
          class="require"
          type="text"
          placeholder="Imie*"
          name="name"
          required
        />
      </div>
      <div class="section-field">
        <input
          id="contact_email"
          v-model="mailData.email"
          class="require"
          type="email"
          placeholder="Email*"
          name="email"
          required
        />
      </div>
      <div class="section-field">
        <input
          id="contact_phone"
          v-model="mailData.phone"
          class="require"
          type="text"
          placeholder="Telefon*"
          name="phone"
          required
        />
      </div>
      <div class="section-field textarea">
        <label for="contact_message"></label>
        <textarea
          id="contact_message"
          v-model="mailData.message"
          class="input-message require"
          placeholder="Wiadomośc*"
          rows="5"
          name="message"
          required
        ></textarea>
      </div>
      <div class="section-field iq-mt-20"></div>
      <button id="submit" name="submit" type="submit" value="Send" @click="onSubmit()">Send Message</button>
      <div id="success" class="alert alert-success alert-dismissible fade show" role="alert">
        <strong>Thank You, Your message has been received.</strong>.
        <button type="button" class="close" data-dismiss="alert" aria-label="Close">
          <span aria-hidden="true">&times;</span>
        </button>
      </div>
    </div>
  </form>
</template>
<script>
export default {
  name: "ContactForm",
  data() {
    return {
      buttonDis: false,
      mailData: {
        name: "",
        email: "",
        phone: "",
        message: ""
      }
    };
  },
  methods: {
    onSubmit($event) {
      console.log(this.mailData.name);
    }
  }
};
</script>
