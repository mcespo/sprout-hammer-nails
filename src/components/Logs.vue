<template>
  <section class="logs">
    <article>
      <h2>The number logs</h2>
      <p>Customers who purchased the wood products of Hammer &amp; Nails saw a marked increase in
lifestyle satisfaction.</p>
    </article>
    <aside>
      <div>
        <h3>65%</h3>
        <p>Ordered our specialty wood from Vermont and are very very very happy</p>
      </div>
      <div>
        <h3>85%</h3>
        <p>Increase in RSVPs to housewarming parties after artisanal tables delivered</p>
      </div>
      <div>
        <h3>10x</h3>
        <p>The results of other competitors in the market because of our quality</p>
      </div>
    </aside>
  </section>
</template>

<script>
export default {
  name: "Logs"
};
</script>

<style scoped lang="scss">
.logs {
  background: transparent url("../assets/section2.jpg") 50% 50% / cover no-repeat;
  @media only screen and (min-width: 960px) {
    background-image: url("../assets/section2@2x.jpg");
  }
}
</style>
