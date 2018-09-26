<template>
  <section class="forests">
    <article class="article-container">
      <h2>The finest from pristine forests</h2>
      <p>We only supply the finest, eco-conscious wood from the most sublime forests of North America, South America and Asia.</p>
    </article>
    <div class="aside-container">
      <aside v-bind:class="{inactive: !showTimber}" @click.prevent="showTimber = true; showFirewood = false" class="timber">
        <svg class="icon" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 82.17 82.17"><path fill="#F3F4F4" d="M41.16 81.17c-21.78 0-39.5-17.72-39.5-39.5s17.72-39.5 39.5-39.5 39.5 17.72 39.5 39.5-17.71 39.5-39.5 39.5zm0-77.01c-20.68 0-37.5 16.82-37.5 37.5s16.82 37.5 37.5 37.5 37.5-16.82 37.5-37.5-16.82-37.5-37.5-37.5z"/><path fill="#F3F4F4" d="M41 54.09c-10.2 0-18.5-8.3-18.5-18.5s8.3-18.5 18.5-18.5 18.5 8.3 18.5 18.5-8.3 18.5-18.5 18.5zm0-35.24c-9.23 0-16.74 7.51-16.74 16.74a16.75 16.75 0 0 0 33.48-.01c0-9.23-7.51-16.73-16.74-16.73z"/><path fill="#F3F4F4" d="M39.92 69.38c-.49 0-1-.43-1-.97V28.97c0-.53.51-.97 1-.97s1 .43 1 .97v39.45c0 .53-.51.96-1 .96z"/><path fill="#F3F4F4" d="M40.46 46.59a.88.88 0 0 1-.52-1.59l8.93-6.49a.88.88 0 0 1 1.04 1.42l-8.93 6.49a.92.92 0 0 1-.52.17zM39.76 40.42a.9.9 0 0 1-.5-.14l-9.14-5.49c-.4-.24-.5-.72-.23-1.07a.96.96 0 0 1 1.22-.2l9.14 5.49c.4.24.5.72.23 1.07a.88.88 0 0 1-.72.34z"/></svg>
        <div>
          <h3>Timber</h3>
          <p>They must be deconstructed meticulously, piece by piece, to preserve the resource until it reaches our mills.</p>
          <a href="#">Learn More</a>
        </div>
      </aside>
      <aside v-bind:class="{inactive: !showFirewood}" @click.prevent="showTimber = false; showFirewood = true" class="firewood">
        <svg class="icon" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 82.17 82.17"><path fill="#F3F4F4" d="M41.16 81.17c-21.78 0-39.5-17.72-39.5-39.5s17.72-39.5 39.5-39.5 39.5 17.72 39.5 39.5-17.71 39.5-39.5 39.5zm0-77.01c-20.68 0-37.5 16.82-37.5 37.5s16.82 37.5 37.5 37.5 37.5-16.82 37.5-37.5-16.82-37.5-37.5-37.5z"/><path fill="#F3F4F4" d="M41 54.09c-10.2 0-18.5-8.3-18.5-18.5s8.3-18.5 18.5-18.5 18.5 8.3 18.5 18.5-8.3 18.5-18.5 18.5zm0-35.24c-9.23 0-16.74 7.51-16.74 16.74a16.75 16.75 0 0 0 33.48-.01c0-9.23-7.51-16.73-16.74-16.73z"/><path fill="#F3F4F4" d="M39.92 69.38c-.49 0-1-.43-1-.97V28.97c0-.53.51-.97 1-.97s1 .43 1 .97v39.45c0 .53-.51.96-1 .96z"/><path fill="#F3F4F4" d="M40.46 46.59a.88.88 0 0 1-.52-1.59l8.93-6.49a.88.88 0 0 1 1.04 1.42l-8.93 6.49a.92.92 0 0 1-.52.17zM39.76 40.42a.9.9 0 0 1-.5-.14l-9.14-5.49c-.4-.24-.5-.72-.23-1.07a.96.96 0 0 1 1.22-.2l9.14 5.49c.4.24.5.72.23 1.07a.88.88 0 0 1-.72.34z"/></svg>
        <div>
          <h3>Firewood</h3>
          <p>Our aim with this line is to raise the bar on the standard American hardwood offering by utilizing extremely selective grading.</p>
          <a href="#">Learn More</a>
        </div>
      </aside>
      <picture v-if="showTimber">
        <source media="(min-width: 960px)" srcset="../assets/tab1@2x.jpg">
        <img src="../assets/tab1.jpg" alt="Image of timber forest">
      </picture>
      <picture v-else-if="showFirewood">
        <source media="(min-width: 960px)" srcset="../assets/tab2@2x.jpg">
        <img src="../assets/tab2.jpg" alt="Image of stacked firewood">
      </picture>
    </div>
  </section>
</template>

<script>
export default {
  name: "Forests",
  data() {
    return {
      showTimber: true,
      showFirewood: false
    };
  }
};
</script>

<style scoped lang="scss">
@import "../scss/_global";

.forests {
  @extend %container-width;
  background-color: $black;
  .article-container {
    @extend %content-centering;
    padding: 80px 0;
    h2 {
      @extend %primary-headline;
      line-height: 1.45;
      @media only screen and (min-width: 960px) {
        line-height: 2.5;
      }
    }
    p {
      @extend %lead-text;
      max-width: 50ch;
    }
  }
  .aside-container {
    display: grid;
    grid-template-areas:
      "aside1"
      "aside2"
      "picture";
      justify-content: center;
    @media only screen and (min-width: 960px) {
      grid-gap: 20px;
      grid-template-columns: repeat(2, 1fr);
      grid-template-areas:
        "aside1 picture"
        "aside2 picture";
    }
    aside {
      cursor: pointer;
      display: grid;
      grid-template-columns: auto 1fr;
      grid-gap: 20px;
    }
    .inactive {
      transition: color 300ms ease-in-out;
      color: $gray-dark;
      svg {
        stroke: $gray-dark;
        path {
          fill: $gray-dark;
        }
      }
      a {
        color: $gray-dark;
      }
    }
    .timber {
      grid-area: aside1;
      padding-bottom: 40px;
      @media only screen and (min-width: 960px) {
        padding: 45px 0 0 0;
      }
    }
    .firewood {
      grid-area: aside2;
      padding-bottom: 80px;
      @media only screen and (min-width: 960px) {
        padding-bottom: 0;
      }
    }
    .icon {
      width: 80px;
    }
    p {
      max-width: 32ch;
    }
    a {
      @extend %learn-more-link;
    }
  }
  picture {
    grid-area: picture;
    justify-self: end;
    max-height: 500px;
    width: 100%;
    max-width: 450px;
    justify-self: center;
    @media only screen and (min-width: 960px) {
      width: auto;
      max-height: 500px;
    }
    img {
      width: 100%;
      @media only screen and (min-width: 960px) {
        width: auto;
        max-height: 500px;
      }
    }
  }
}
</style>
