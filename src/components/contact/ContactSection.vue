<template>
  <!-- <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 496 512"><
        !--! Font Awesome Pro 6.2.0 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2022 Fonticons, Inc. -->
  <!-- <path d="M248,8C111.033,8,0,119.033,0,256S111.033,504,248,504,496,392.967,496,256,384.967,8,248,8ZM362.952,176.66c-3.732,39.215-19.881,134.378-28.1,178.3-3.476,18.584-10.322,24.816-16.948,25.425-14.4,1.326-25.338-9.517-39.287-18.661-21.827-14.308-34.158-23.215-55.346-37.177-24.485-16.135-8.612-25,5.342-39.5,3.652-3.793,67.107-61.51,68.335-66.746.153-.655.3-3.1-1.154-4.384s-3.59-.849-5.135-.5q-3.283.746-104.608,69.142-14.845,10.194-26.894,9.934c-8.855-.191-25.888-5.006-38.551-9.123-15.531-5.048-27.875-7.717-26.8-16.291q.84-6.7,18.45-13.7,108.446-47.248,144.628-62.3c68.872-28.647,83.183-33.623,92.511-33.789,2.052-.034,6.639.474,9.61,2.885a10.452,10.452,0,0,1,3.53,6.716A43.765,43.765,0,0,1,362.952,176.66Z"/></svg> -->
  <div class="contact">
    <h2 class="heading" id="contact">Elevator <span>Pitch</span></h2>
    <div>
      <p>"Hello! I'm a passionate professional from Amazon Web Services (AWS), where I've honed my expertise in cloud computing and cutting-edge technologies. With a proven track record of driving innovation and delivering impactful solutions, I specialize in architecting scalable, secure, and high-performance cloud infrastructures that empower businesses to thrive in the digital era. My deep understanding of AWS services, coupled with my commitment to staying at the forefront of industry trends, ensures I can effectively design, implement, and optimize cloud solutions tailored to your specific needs. Let's collaborate to elevate your company's capabilities and unlock new opportunities for growth in the dynamic world of cloud computing."</p>
      <!-- <form
        action="mailto:tibesolomon7@gmail.com"
        method="get"
        enctype="text/plain"
      >
        <label class="label" for="subject">Subject</label>
        <input
          class="input"
          name="subject"
          type="text"
          placeholder="..."
          v-model.trim="subject"
        />
        <label class="label" for="phone">Phone Number</label>
        <input
          class="input"
          name="phone"
          id="phone"
          type="tel"
          placeholder="..."
          v-model.number="phone"
        />
        <label class="label" for="message">Message</label>
        <textarea
          class="input"
          name="BODY"
          placeholder="..."
          id="message"
          cols="30"
          rows="10"
        ></textarea>

        <base-button type="submit"> Send Message </base-button>
      </form> -->
    </div>
    <iframe width="560" height="315" src="https://www.youtube.com/embed/wkrMZPUGVho" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
  </div>
</template>

<script>
// import BaseButton from "../UI/BaseButton.vue";
import store from "../../store";

export default {
  components: {
    // BaseButton,
  },
  data() {
    return {
      email: null,
      subject: null,
      phone: null,
      message: null,
    };
  },
  methods: {
    sendMessage() {
      console.log(this.$el.querySelector("span").style.color);
      console.log("object");
      store.set("darkTheme", true);
      console.log(store.get("theme"));
      // console.log(store.get("theme"))
      // console.log(store.remove("theme"));
      // console.log(store.clearAll())
      console.log(store.state());
      // console.log(store.localStorage)
      // console.log([this.email, this.subject, this.phone,this.message]);
    },
  },
};
</script>

<style scoped>
/* svg{
    transform:scale(0.1);
} */

.label {
  font-size: 2rem;
  color: var(--green);
  border: 1rem solid transparent;
  text-shadow: var(--box-shadow-inset);
}
.contact {
  padding-bottom: 11rem;
}
form {
  margin: 1rem auto;
  max-width: 70rem;
  border-radius: 0.5rem;
  box-shadow: var(--box-shadow);
  padding: 2rem;
  text-align: left;
}
.input {
  padding: 1rem 1.5rem;
  width: 100%;
  background: none;
  color: var(--black);
  font-size: 1.6rem;
  text-transform: none;
  margin: 0.7rem 0;
  box-shadow: var(--box-shadow);
  border-radius: 0.5rem;
}
.input:focus {
  box-shadow: var(--box-shadow-inset);
}
textarea {
  height: 20rem;
  resize: none;
}
</style>
