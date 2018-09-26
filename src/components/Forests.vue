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
        <svg class="icon" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 82.17 82.17"><path fill="#F3F4F4" d="M41.09 80.59a39.55 39.55 0 0 1-39.5-39.5c0-21.78 17.72-39.5 39.5-39.5s39.5 17.72 39.5 39.5a39.55 39.55 0 0 1-39.5 39.5zm0-77.01c-20.68 0-37.5 16.82-37.5 37.5s16.82 37.5 37.5 37.5 37.5-16.82 37.5-37.5-16.83-37.5-37.5-37.5z"/><path fill="#F3F4F4" d="M41.92 70.32c-.49 0-1-.43-1-.97V29.9c0-.53.51-.97 1-.97s1 .43 1 .97v39.45c0 .53-.51.97-1 .97z"/><path fill="#F3F4F4" d="M42.32 48.4a.86.86 0 0 1-.73-.42 1.1 1.1 0 0 1 .2-1.41l9.1-7.44c.4-.33.96-.23 1.25.22.29.45.2 1.08-.2 1.41l-9.1 7.44a.76.76 0 0 1-.52.2zM41.64 41.26a.84.84 0 0 1-.45-.13L33 35.71a.74.74 0 0 1-.2-1.06.82.82 0 0 1 1.1-.2l8.2 5.42c.36.24.45.71.2 1.06a.8.8 0 0 1-.66.33z"/><path fill="#F3F4F4" d="M41.78 61.26l-.17-.01c-.17-.03-16.68-2.98-15.69-22.73.98-19.5 14.88-25.28 15.48-25.51.52-.21 1.12.04 1.33.55a1 1 0 0 1-.56 1.3c-.03.01-3.37 1.39-6.77 4.99-4.55 4.82-7.05 11.14-7.44 18.77-.9 17.94 13.38 20.55 13.99 20.66a1 1 0 0 1-.17 1.98z"/><path fill="#F3F4F4" d="M42.7 61.26c-.49 0-.92-.35-1-.83a1 1 0 0 1 .84-1.15c.62-.1 14.89-2.73 13.99-20.66-.93-18.24-14.09-23.71-14.22-23.76a1 1 0 0 1-.56-1.3c.21-.51.8-.76 1.33-.55.59.24 14.5 6.02 15.47 25.52.99 19.75-15.52 22.7-15.69 22.73h-.16z"/></svg>
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
      h3 {
        color: $tussock;
        text-transform: uppercase;
        font-size: 14px;
      }
    }
    .inactive {
      transition: color 300ms ease-in-out;
      color: $gray-dark;
      h3, a {
        color: $gray-dark;
      }
      svg {
        stroke: $gray-dark;
        path {
          fill: $gray-dark;
        }
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
      margin-bottom: 20px;
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
