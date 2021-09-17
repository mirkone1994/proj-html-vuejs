<template>
  <div id="app">
    <Header/>
    <Main/>
    <Footer/>
  </div>
</template>

<script>
import Header from "./components/Header.vue"
import Main from "./components/Main.vue"
import Footer from "./components/Footer.vue"
export default {
  name: 'App',
  components: {
    Header,
    Main,
    Footer,
  }
}
</script>

<style lang="scss">
@import "scss/style.scss";
@import "~@fortawesome/fontawesome-free/css/all.min.css";
.mt-10{
    margin-top: 150px;
}
.mb-10{
    margin-bottom: 150px;
}
.pt-10 {
  padding-top: 100px;
}
.pr {
  position: relative;
}
.bg-almostgreen {
  background-color: #eef4ed;
}
.txt-lightgreen {
  color: $light-green;
}
.bg-lightgreen {
  background-color: $light-green;
}
.bg-darkgreen {
  background-color: #0e272d;
}
.txt-green {
  color: $dark-green;
}
.bg-green {
  background-color: $dark-green;
}

</style>
