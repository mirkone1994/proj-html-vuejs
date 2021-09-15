<template>
  <div class="header">
    <div id="htop" class="container-fluid">
      <div class="container">
        <div class="row justify-content-between">
          <div class="col d-flex align-items-center">
            <span><i class="fas fa-clock"></i> Open Hours: Mon - Sat - 9.00 - 18.00</span>
          </div>
          <div class="col d-flex justify-content-end align-items-center">
            <ul>
              <li><i class="fas fa-phone-alt"> +1 (305) 1234-5678</i></li>
              <li><i class="fas fa-envelope"> hello@example.com</i></li>
              <li v-for="(contact, i) in hContacts" :key="i">
                <i :class="hContacts[i]"></i>
              </li>
            </ul>
          </div>
        </div>
      </div>
    </div>
    <div id="hbot" class="container-fluid">
      <div class="container py-5">
        <div class="row justify-content-between">
            <div class="col-2">
                <span id="NEX">NEX</span><span>GEN</span>
            </div>
            <div class="col d-flex justify-content-end">
                <ul>
                    <li v-for="(link, i) in hLinks" :key="i">{{hLinks[i]}}</li>
                    <li><i class="far fa-user"></i></li>
                    <li id="GIT">GET IN TOUCH</li>
                </ul>
            </div>
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
      hLinks: ['HOME', "ABOUT", "SERVICES", "PROCESS", "TESTIMONIALS"],
    };
  },
};
</script>

<style scoped lang="scss">
.header {
    color: #fff;
}
#htop {
    background-color: #21333e;
}
ul {
  list-style: none;
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
}
#NEX {
    background-color: #05838369;
    padding: 10px 0px 10px 20px;
    color: #00a4a4;
    border-top-left-radius: 30px;
    border-bottom-left-radius: 30px;
}
#GIT {
    background-color: #058283;
    ruby-span: 15px 10px;
    border-radius: 3px;
}
</style>