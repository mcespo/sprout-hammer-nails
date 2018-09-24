<template>
  <div id="app">
    <Navbar />
    <!-- <img alt="Vue logo" src="./assets/logo.png"> -->
    <HelloWorld msg="Bespoke Wood Products"/>
  </div>
</template>

<script>
import Navbar from "./components/Navbar.vue";
import HelloWorld from "./components/HelloWorld.vue";

export default {
  name: "app",
  components: {
    Navbar,
    HelloWorld
  }
};
</script>

<style lang="scss">
@import url("https://p.typekit.net/p.css?s=1&k=pmy1mon&ht=tk&f=139.169.175&a=14567271&app=typekit&e=css");

@font-face {
  font-family: "proxima-nova";
  src: url("https://use.typekit.net/af/71f83c/00000000000000003b9b093b/27/l?primer=bdc973ea9945bf2ee2550957b401916e56fc5fc4cec4e29110795767e60d6b9a&fvd=n7&v=3") format("woff2"), url("https://use.typekit.net/af/71f83c/00000000000000003b9b093b/27/d?primer=bdc973ea9945bf2ee2550957b401916e56fc5fc4cec4e29110795767e60d6b9a&fvd=n7&v=3") format("woff"), url("https://use.typekit.net/af/71f83c/00000000000000003b9b093b/27/a?primer=bdc973ea9945bf2ee2550957b401916e56fc5fc4cec4e29110795767e60d6b9a&fvd=n7&v=3") format("opentype");
  font-style: normal;
  font-weight: 700;
}

@font-face {
  font-family: "proxima-nova";
  src: url("https://use.typekit.net/af/a3eee8/00000000000000003b9b093c/27/l?primer=bdc973ea9945bf2ee2550957b401916e56fc5fc4cec4e29110795767e60d6b9a&fvd=n8&v=3") format("woff2"), url("https://use.typekit.net/af/a3eee8/00000000000000003b9b093c/27/d?primer=bdc973ea9945bf2ee2550957b401916e56fc5fc4cec4e29110795767e60d6b9a&fvd=n8&v=3") format("woff"), url("https://use.typekit.net/af/a3eee8/00000000000000003b9b093c/27/a?primer=bdc973ea9945bf2ee2550957b401916e56fc5fc4cec4e29110795767e60d6b9a&fvd=n8&v=3") format("opentype");
  font-style: normal;
  font-weight: 800;
}

@font-face {
  font-family: "proxima-nova";
  src: url("https://use.typekit.net/af/4838bd/00000000000000003b9b0934/27/l?primer=bdc973ea9945bf2ee2550957b401916e56fc5fc4cec4e29110795767e60d6b9a&fvd=n4&v=3") format("woff2"), url("https://use.typekit.net/af/4838bd/00000000000000003b9b0934/27/d?primer=bdc973ea9945bf2ee2550957b401916e56fc5fc4cec4e29110795767e60d6b9a&fvd=n4&v=3") format("woff"), url("https://use.typekit.net/af/4838bd/00000000000000003b9b0934/27/a?primer=bdc973ea9945bf2ee2550957b401916e56fc5fc4cec4e29110795767e60d6b9a&fvd=n4&v=3") format("opentype");
  font-style: normal;
  font-weight: 400;
}

* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

#app {
  font-family: "proxima-nova", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}
</style>
