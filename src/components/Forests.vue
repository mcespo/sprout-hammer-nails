<template>
  <section class="forests">
    <article class="article-container">
      <h2>The finest from pristine forests</h2>
      <p>We only supply the finest, eco-conscious wood from the most sublime forests of North America,
South America and Asia.</p>
    </article>
    <div class="aside-container">
      <aside>
        <div>
          <!-- svg -->
          <h3>Timber</h3>
          <p>They must be deconstructed meticulously, piece by piece, to preserve the resource until it reaches our mills.</p>
          <a href="#">Learn More</a>
        </div>
        <!-- svg -->
      </aside>
      <aside>
        <!-- svg -->
        <div>
          <h3>Firewood</h3>
          <p>Our aim with this line is to raise the bar on the standard American hardwood offering by utilizing extremely selective grading.</p>
          <a href="#">Learn More</a>
        </div>
        <!-- svg -->
      </aside>
      <!-- <img src="" alt=""> -->
    </div>
    <!-- <img src="" alt="">
    <img src="" alt=""> -->
  </section>
</template>

<script>
export default {
  name: "Forests"
};
</script>

<style scoped lang="scss">
@import "../scss/_global";

.forests {
  background-color: $black;
  .article-container {
    padding: 80px 0;
  }
}
</style>
