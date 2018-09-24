<template>
  <section class="woodworking">
    <div class="article-container">
      <article>
        <h2>The art of woodworking</h2>
        <p>Woodworking is an austere art and here at Hammer &amp; Nails we see ourselves as wood curators
  and artists. Bespoke quality wood, the finest artisanal touches mark our work from start to finish.
  Nate Turner is the mastercraftsman behind it all.</p>
      </article>
      <img src="../assets/craftsman.jpg" alt="">
    </div>
    <div class="aside-container">
      <aside>
        <h3>Bespoke</h3>
        <h4>The styles represented in this line are quite simply here to stay</h4>
        <p>They must be deconstructed meticulously, piece by piece, to preserve the resource until it
reaches our mills.</p>
        <a href="#">Learn More</a>
      </aside>
      <aside>
        <h3>Handcrafted]</h3>
        <h4>Perhaps the best term to describe these woods is timeless</h4>
        <p>Oak reacts beautifully to our custom staining process, yielding colors that simply are not possible
to attain on American Oak.</p>
        <a href="#">Learn More</a>
      </aside>
      <aside>
        <h3>Artisinal</h3>
        <h4>These ancient and abandoned American timbers find a new life</h4>
        <p>Our aim with this line is to raise the bar on the standard American hardwood offering by utilizing
extremely selective grading.</p>
        <a href="#">Learn More</a>
      </aside>
    </div>
  </section>
</template>

<script>
export default {
  name: "Woodworking"
};
</script>

<style scoped lang="scss">
@import "../scss/_global";

.woodworking {
  background-color: $gray-darker;
  .article-container {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    justify-content: space-around;
    padding: 5em 0;
    background: transparent url("../assets/section1.jpg") 50% 50% / cover no-repeat;
    @media only screen and (min-width: 960px) {
      background-image: url("../assets/section1@2x.jpg");
    }
  }
  .aside-container {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    justify-content: space-around;
  }
}
</style>
