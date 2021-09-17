<template>
  <div class="container-fluid bg-darkblue py-5 text-center text-light">
    <div class="container py-5">
      <span class="d-block txt-green fw-bold mb-4">CUSTOMER TESTIMONIALS</span>
      <h2 class="mb-4 fw-bold">
        Trusted <span class="bg-darkgreen p-1">Feedback</span>
      </h2>
      <p class="txt-silver">
        We work intesively in search of ideals that can add up in the lives of
        our customers. This is what <br />moves us and we are grateful for the
        recognition.
      </p>
    </div>
    <div class="row justify-content-evenly">
      <div
        v-for="feedback in feedbakcs"
        :key="feedback.id"
        class="col-2 services-card text-start mb-5"
      >
        <i class="fas fa-quote-right fs-4"></i>
        <img class="w-50 px-3 pt-4 filtered" :src="feedback.img" alt="" />
        <p class="my-3 px-3 txt-silver">{{ feedback.overview }}</p>
        <span class="d-block px-3 pb-4 txt-silver">{{ feedback.lorem }}</span>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Feedback",
  data() {
    return {
      feedbakcs: [
        {
          img: require("@/img/logo-1.png"),
          lorem: "Lorem ipsum dolor sit armet, consectetur adipiscing elit.",
          overview:
            "Praesent volutpat justo sit amet elementum malesuada. Praesent sagittis augue justo, in accumsan orci rhoncus at pellentesque.",
          id: 1,
        },
        {
          img: require("@/img/logo-2.png"),
          lorem: "Lorem ipsum dolor sit armet, consectetur adipiscing elit.",
          overview:
            "Praesent volutpat justo sit amet elementum malesuada. Praesent sagittis augue justo, in accumsan orci rhoncus at pellentesque.",
          id: 2,
        },
        {
          img: require("@/img/logo-3.png"),
          lorem: "Lorem ipsum dolor sit armet, consectetur adipiscing elit.",
          overview:
            "Praesent volutpat justo sit amet elementum malesuada. Praesent sagittis augue justo, in accumsan orci rhoncus at pellentesque.",
          id: 3,
        },
      ],
    };
  },
};
</script>

<style>
.filtered {
  filter: invert(100%);
}
.fa-quote-right {
  position: absolute;
  bottom: 25px;
  right: 25px;
}
</style>