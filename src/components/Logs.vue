<template>
  <section class="logs">
    <article>
      <h2>The number logs</h2>
      <p>Customers who purchased the wood products of Hammer &amp; Nails saw a marked increase in
lifestyle satisfaction.</p>
    </article>
    <div class="aside-container">
      <aside>
        <h3>65%</h3>
        <p>Ordered our specialty wood from Vermont and are very very very happy</p>
      </aside>
      <aside>
        <h3>85%</h3>
        <p>Increase in RSVPs to housewarming parties after artisanal tables delivered</p>
      </aside>
      <aside>
        <h3>10x</h3>
        <p>The results of other competitors in the market because of our quality</p>
      </aside>
    </div>
  </section>
</template>

<script>
export default {
  name: "Logs"
};
</script>

<style scoped lang="scss">
@import "../scss/_global";

.logs {
  background: transparent url("../assets/section2.jpg") 50% 50% / cover no-repeat;
  @media only screen and (min-width: 960px) {
    background-image: url("../assets/section2@2x.jpg");
  }
}
</style>
