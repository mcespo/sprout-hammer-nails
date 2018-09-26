<template>
  <div id="app">
    <Navbar />
    <Header id="page-wrap" />
    <Woodworking />
    <Logs />
    <Forests />
    <Customers />
    <Footer />
  </div>
</template>

<script>
import Navbar from "./components/Navbar.vue";
import Header from "./components/Header.vue";
import Woodworking from "./components/Woodworking.vue";
import Logs from "./components/Logs.vue";
import Forests from "./components/Forests.vue";
import Customers from "./components/Customers.vue";
import Footer from "./components/Footer.vue";

export default {
  name: "app",
  components: {
    Navbar,
    Header,
    Woodworking,
    Logs,
    Forests,
    Customers,
    Footer
  }
};
</script>

<style lang="scss">
@import "./scss/_global";
</style>
