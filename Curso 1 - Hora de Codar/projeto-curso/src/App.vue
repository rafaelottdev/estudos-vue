<template>
  <Navbar :logo="logo_src" :alt="app_name" />
  <RouterView />
  <Footer />
</template>

<script>
import Navbar from './components/Navbar.vue'
import Footer from './components/Footer.vue'

  export default {
    components: {
      Navbar, Footer
    },
    data() {
      return {
        logo_src: "/img/logo.png",
        app_name: "Make your Burguer"
      }
    }
  }
</script>

<style>
  * {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: Helvetica;
  }
  .main-container {
    min-height: 250px;
    margin: 50px;
  }
  h1 {
    margin-bottom: 30px;
    text-align: center;
    font-size: 42px;
    color: #222;
  }
</style>