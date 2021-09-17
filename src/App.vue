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

</style>
