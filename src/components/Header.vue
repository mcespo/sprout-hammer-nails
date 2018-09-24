<template>
  <header class="header">
    <h1>Bespoke Wood Products?</h1>
    <p>Inventive design coupled with skilled craftsmanship and advanced machinery<br>
    result in high quality finished product by mastercraftsman Nate Turner.</p>
    <a class="cta" href="#">Request More Info</a>
  </header>
</template>

<script>
export default {
  name: "Header"
};
</script>

<style scoped lang="scss">
@import "../scss/_global";

.header {
  padding: 12em 0;
  display: grid;
  justify-items: center;
  align-items: center;
  text-align: center;
  background: transparent url("../assets/hero.jpg") 50% 50% / cover no-repeat;
  @media only screen and (min-width: 960px) {
    background-image: url("../assets/hero@2x.jpg");
  }
  h1 {
    font-weight: 800;
    font-size: 5em;
    line-height: 1;
  }
  p {
    padding: 2em 0 3em;
  }
  .cta {
    min-width: 18em;
  }
}
</style>
