<template>
  <div id="app">
    <Header />
    <Main />
    <Footer />
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import Main from "./components/Main.vue";
import Footer from "./components/Footer.vue";
export default {
  name: "App",
  components: {
    Header,
    Main,
    Footer,
  },
};
</script>

<style lang="scss">
@import "scss/style.scss";
@import "~@fortawesome/fontawesome-free/css/all.min.css";
//position
.mt-10 {
  margin-top: 150px;
}
.mb-10 {
  margin-bottom: 150px;
}
.pt-10 {
  padding-top: 100px;
}
.pr {
  position: relative;
}
//utilities
ul {
  list-style: none;
}
#NEX {
  background-color: #05838369;
  padding: 5px 0px 5px 20px;
  color: $green;
  border-top-left-radius: 30px;
  border-bottom-left-radius: 30px;
}
//colors
.bg-almostgreen {
  background-color: $almost-green;
}
.txt-lightgreen {
  color: $light-green;
}
.bg-lightgreen {
  background-color: $light-green;
}
.bg-darkgreen {
  background-color: $dark-green;
}
.txt-green {
  color: $green;
}
.bg-green {
  background-color: $green;
}
.bg-darkblue {
  background-color: $dark-blue;
}
</style>
