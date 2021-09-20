<template>
  <div class="header text-light">
    <div id="htop" class="container-fluid txt-silver">
      <div class="container">
        <div class="row justify-content-between">
          <div class="col d-flex align-items-center">
            <span
              ><i class="fas fa-clock"></i> Open Hours: Mon - Sat - 9.00 -
              18.00</span
            >
          </div>
          <div class="col d-flex justify-content-end mt-2 align-items-center">
            <ul>
              <li>
                <i class="fas fa-phone-alt"
                  ><a class="text-light" href=""> +1 (305) 1234-5678</a>
                </i>
              </li>
              <li>
                <i class="fas fa-envelope"
                  ><a class="text-light" href=""> hello@example.com</a></i
                >
              </li>
              <li v-for="(contact, i) in hContacts" :key="i">
                <a class="text-light" href=""><i :class="hContacts[i]"></i></a>
              </li>
            </ul>
          </div>
        </div>
      </div>
    </div>
    <div id="hbot" class="container-fluid resetp">
      <div id="bg-darkness">
        <div class="container py-5">
          <div class="row justify-content-between fs-5 fw-bold">
            <div class="col-2"><span id="NEX">NEX</span><span> GEN</span></div>
            <div class="col d-flex justify-content-end">
              <ul>
                <li v-for="(link, i) in hLinks" :key="i">
                  <a class="text-light" href="">{{ hLinks[i] }}</a>
                </li>
                <li><i class="far fa-user"></i></li>
                <li id="GIT"><a class="text-light" href="">GET IN TOUCH</a></li>
              </ul>
            </div>
          </div>
        </div>
        <div class="container my-5">
          <span class="d-block fw-bold mt-10 txt-green"
            >LOGISTICS SERVICES</span
          >
          <span class="fs-70 fw-bold">CARGO<br />TRANSPORT</span>
          <p class="my-4 txt-silver">
            Fractional exclusive road transportationto all<br />regions, with
            small, medium and large vehicles
          </p>
          <span id="GIT"><a class="text-light" href="">GET IN TOUCH</a> </span>
          <span id="RM"><a class="text-light" href="">READ MORE</a></span>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Header",
  data() {
    return {
      hContacts: ["fab fa-facebook-f", "fab fa-twitter", "fab fa-linkedin-in"],
      hLinks: ["HOME", "ABOUT", "SERVICES", "PROCESS", "TESTIMONIALS"],
    };
  },
};
</script>

<style scoped lang="scss">
@import "../scss/style.scss";
a {
  text-decoration: none;
}
#htop {
  background-color: #21333e;
}
li {
  display: inline;
  padding: 0 20px;
}
#hbot {
  background-image: url(../img/bg-9.jpg);
  height: 1064px;
  background-repeat: no-repeat;
  background-size: cover;
  padding-right: 0;
  padding-left: 0;
}
#bg-darkness {
  background-color: rgba($color: #000000, $alpha: 0.5);
  height: 100%;
}
.fs-70 {
  font-size: 70px;
}
#GIT {
  background-color: $green;
  padding: 10px 15px;
  border-radius: 3px;
}
#RM {
  border: 1px solid $green;
  padding: 10px 15px;
  border-radius: 3px;
  margin-left: 40px;
}
</style>