<template>
  <header class="header">
    <h1>Bespoke Wood Products?</h1>
    <p>Inventive design coupled with skilled craftsmanship and advanced machinery result in high quality finished product by mastercraftsman Nate Turner.</p>
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
  @extend %content-centering;
  padding: 14em 0 12em;
  background: transparent url("../assets/hero.jpg") 50% 50% / cover no-repeat;
  @media only screen and (min-width: 960px) {
    background-image: url("../assets/hero@2x.jpg");
  }
  h1 {
    @extend %huge-headline;
    line-height: 1;
  }
  p {
    @extend %lead-text;
    @extend %content-centering;
    max-width: 56ch;
    padding: 2em 5vw 3em;
    @media only screen and (min-width: 960px) {
      padding-left: 0;
      padding-right: 0;
    }
  }
  .cta {
    min-width: 18em;
  }
}
</style>
