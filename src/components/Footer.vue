<template>
  <div class="container-fluid resetp">
    <div id="ftop" class="container mt-10 mb-10">
      <div class="row">
        <div class="col-7">
          <span class="d-block txt-green fw-bold">SEND A MESSAGE</span>
          <h2 class="fw-bold my-5">
            Get in <span class="txt-green bg-lightgreen p1">Touch</span>
          </h2>
          <p class="mb-5">
            We will respond to your message as soon as possible.
          </p>
          <Form />
        </div>
        <div class="col-5">
          <h3 class="fw-bold">Example Inc.</h3>
          <p class="mt-5">
            Lorem ipsum, dolor sit amet consectetur adipisicing elit. Lorem
            ipsum, dolor sit amet consectetur adipisicing elit.
          </p>
          <p class="mb-5">
            Lorem ipsum, dolor sit amet consectetur adipisicing elit. Lorem
            ipsum, dolor sit amet consectetur adipisicing elit.
          </p>
          <ul>
            <li class="my-4" v-for="contact in contacts" :key="contact.id">
              <i
                class="rounded-circle txt-green bg-lightgreen p-3"
                :class="contact.img"
              ></i
              ><span class="txt-green"> {{ contact.contact }}</span>
            </li>
          </ul>
          <span id="VM" class="txt-green mt-5">VIEW MAP</span>
        </div>
      </div>
    </div>
    <div id="fbot" class="bg-darkblue container-fluid text-light">
      <div class="container py-5">
        <div class="row justify-content-evenly">
          <div class="col-3">
            <span class="fs-3 fw-bold"><span id="NEX">NEX</span> GEN</span>
            <p class="mt-4 txt-silver">
              A functional HTML Template <br />
              for Corporate & Business
            </p>
            <ul>
              <li class="my-4" v-for="contact in contacts" :key="contact.id">
                <i class="" :class="contact.img"></i
                ><span class="txt-silver"> {{ contact.contact }}</span>
              </li>
            </ul>
            <span id="GIT">GET IN TOUCH</span>
          </div>
          <div
            v-for="title in titles"
            :key="title.id"
            class="col-2 py-4 links-card"
          >
            <span class="fs-3 ps-4 fw-bold">{{ title.title }}</span>
            <ul class="mt-2">
              <li
                id="links"
                class="my-1 txt-silver"
                v-for="link in links"
                :key="link"
              >
                <i class="fas fa-chevron-right"></i> {{ link }}
              </li>
            </ul>
          </div>
        </div>
      </div>
      <div
        class="
          hend
          row
          bg-black
          text-light
          align-items-center
          justify-content-between
        "
      >
        <div class="col-1 offset-1"></div>
        <div class="col-4 text-center txt-silver">
          Enjoy the low price. We are tracking any intention of piracy.
        </div>
        <div class="col-4 text-center txt-silver">
          2020 NEXGEN is Proudly Powered by
          <span class="txt-green">Codings</span>.
        </div>
        <div class="col-1">
          <a id="scrolltop" href="top"
            ><i class="fas fa-arrow-alt-circle-up fa-2x"></i
          ></a>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Form from "./Form.vue";
export default {
  name: "Footer",
  components: {
    Form,
  },
  data() {
    return {
      contacts: [
        {
          img: "fas fa-phone-alt",
          contact: "+1 (305) 1234 5678",
          id: 1,
        },
        {
          img: "fas fa-envelope",
          contact: "hello@example.com",
          id: 2,
        },
        {
          img: "fas fa-map-marker-alt",
          contact: "Main Avenue, 987",
          id: 3,
        },
      ],
      titles: [
        {
          id: 1,
          title: "About",
        },
        {
          id: 2,
          title: "Transport",
        },
        {
          id: 3,
          title: "Support",
        },
      ],
      links: [
        "The Company",
        "Insitutional",
        "Social & Events",
        "Innovation",
        "Enviroment",
        "Technology",
      ],
    };
  },
};
</script>

<style scoped lang="scss">
@import "../scss/style.scss";
.resetp {
  padding-right: 0;
  padding-left: 0;
}
li {
  margin-left: -30px;
}
#links {
  margin-left: -8px;
}
#VM {
  border: 1px solid $green;
  padding: 10px 15px;
  border-radius: 3px;
}
#GIT {
  border: 1px solid $green;
  padding: 10px 15px;
  border-radius: 3px;
}
.links-card {
  background-color: #19191f;
  border-radius: 15px;
}
.hend {
  font-size: 0.75em;
  height: 50px;
}
#scrolltop {
  color: grey;
}
</style>