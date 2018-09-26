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
    @media only screen and (min-width: 960px) {
      grid-template-columns: repeat(3, 1fr);
      grid-gap: 40px;
      padding: 80px 0;
    }
    aside {
      padding: 20px 0;
      @media only screen and (min-width: 960px) {
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
    }
    h3 {
      @extend %primary-headline;
      color: $tussock;
    }
    p {
      @extend %lead-text;
      max-width: 30ch;
      margin: 0 auto;
      @media only screen and (min-width: 960px) {
        margin: 0;
      }
    }
  }
}
</style>
