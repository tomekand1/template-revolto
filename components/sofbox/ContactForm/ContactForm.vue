<template>
  <form method="post" @submit.prevent="onSubmit($event)" autocomplete="off">
    <div class="contact-form">
      <div class="section-field">
        <input
          id="contact_name"
          v-model="mailData.name"
          class="require"
          type="text"
          placeholder="Imię*"
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
          placeholder="Mail*"
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
          placeholder="Wiadomość*"
          rows="5"
          name="message"
          required
        ></textarea>
      </div>

      <button
        id="submit"
        name="submit"
        type="submit"
        value="Send"
        :class="buttonDis ? 'button iq-mt-15 disabled' : 'button iq-mt-15 '"
      >Wyślij</button>
    </div>
  </form>
</template>

<script>
import axios from "axios";

export default {
  name: "ContactForm",
  data() {
    return {
      buttonDis: true,
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
      axios
        .post(`${process.env.baseUrl}/api/mail`, this.mailData)
        .then(res => {
          swal({
            title: "Email został pomyślnie wysłany.",
            icon: "success",
            button: "ok"
          });
          this.clearData();
        })
        .catch(console.error());
    },
    clearData() {
      this.mailData.name = "";
      this.mailData.email = "";
      this.mailData.phone = "";
      this.mailData.message = "";
    }
  }
};
</script>
