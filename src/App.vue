<template>
  <div id="app">
    <!-- <img alt="Vue logo" src="./assets/logo.png"> -->
    <Navbar />
    <Header />
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
@import url("https://p.typekit.net/p.css?s=1&k=pmy1mon&ht=tk&f=139.169.175&a=14567271&app=typekit&e=css");
@import "./scss/_global";

#app {
  font-family: "proxima-nova", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: $white;
}

.cta {
  text-decoration: none;
  padding: 15px 20px;
  font-weight: 700;
  color: $white;
  background-color: $pomegranate;
}
</style>
