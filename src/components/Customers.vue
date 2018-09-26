<template>
  <section class="customers">
    <div class="container">
      <h3>Esteemed and worthy customers</h3>
      <ul class="sponsor-logos">
        <img src="../assets/logo_bcbsla.svg" alt="">
        <img src="../assets/logo_gvc-mortgage.svg" alt="">
        <img src="../assets/logo_hazeldon-betty-ford2.svg" alt="">
        <img src="../assets/logo_mutual-mortgage.svg" alt="">
        <img src="../assets/logo_zendesk.svg" alt="">
        <img style="height:140px;" src="../assets/logo_city-of-las-vegas2.svg" alt="">
      </ul>
    </div>
  </section>
</template>

<script>
export default {
  name: "Customers"
};
</script>

<style scoped lang="scss">
@import "../scss/_global";

.customers {
  background-color: $gray-darker;
  .container {
    @extend %container-width;
    padding: 100px 0;
    h3 {
      @extend %content-centering;
      @extend %small-title;
    }
    .sponsor-logos {
      display: grid;
      grid-gap: 20px;
      align-items: center;
      justify-content: center;
      grid-template-columns: repeat(2, 1fr);
      @media only screen and (min-width: 960px) {
        grid-template-columns: repeat(6, 1fr);
      }
      img {
        justify-self: center;
        width: 140px;
        height: 120px;
      }
    }
  }
}
</style>
