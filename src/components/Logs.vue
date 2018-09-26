<template>
  <section class="logs">
    <article class="article-container">
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
  padding: 80px 0;
  text-align: center;
  background: transparent url("../assets/section2.jpg") 50% 50% / cover no-repeat;
  @media only screen and (min-width: 960px) {
    background-image: url("../assets/section2@2x.jpg");
  }
  .article-container {
    @extend %content-centering;
    & > *:not(:last-child) {
      @extend %container-width;
    }
    h2 {
      @extend %primary-headline;
      line-height: 2.5;
    }
    p {
      @extend %lead-text;
      max-width: 50ch;
    }
  }
  .aside-container {
    @extend %container-width;
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    grid-gap: 40px;
    padding: 80px 0;
    aside {
      &:first-child {
        justify-self: start;
      }
      &:nth-child(2) {
        justify-self: center;
      }
      &:last-child{
        justify-self: end;
      }
    }
    padding-top: 60px;
    h3 {
      color: $tussock;
      font-weight: 800;
      font-size: between(20px, 43px, 100px, 959px);
      @media only screen and (min-width: 960px) {
        font-size: between(44px, 60px, 960px, 1400px);
      }
    }
    p {
      @extend %lead-text;
      max-width: 30ch;
    }
  }
}
</style>
