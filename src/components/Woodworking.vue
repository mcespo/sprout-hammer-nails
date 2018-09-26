<template>
  <section class="woodworking">
    <div class="article-container">
      <article>
        <h2>The art of woodworking</h2>
        <p>Woodworking is an austere art and here at Hammer &amp; Nails we see ourselves as wood curators
  and artists. Bespoke quality wood, the finest artisanal touches mark our work from start to finish.
  Nate Turner is the mastercraftsman behind it all.</p>
      </article>
      <picture>
        <source media="(min-width: 960px)" srcset="../assets/craftsman@2x.jpg">
        <img src="../assets/craftsman.jpg" alt="image of Nate Turner">
      </picture>
    </div>
    <div class="aside-bg">
      <div class="aside-container">
      <aside>
        <h3>Bespoke</h3>
        <h4>The styles represented in this line are quite simply here to stay</h4>
        <p>They must be deconstructed meticulously, piece by piece, to preserve the resource until it reaches our mills.</p>
        <a href="#">Learn More</a>
      </aside>
      <aside>
        <h3>Handcrafted</h3>
        <h4>Perhaps the best term to describe these woods is timeless</h4>
        <p>Oak reacts beautifully to our custom staining process, yielding colors that simply are not possible to attain on American Oak.</p>
        <a href="#">Learn More</a>
      </aside>
      <aside>
        <h3>Artisinal</h3>
        <h4>These ancient and abandoned American timbers find a new life</h4>
        <p>Our aim with this line is to raise the bar on the standard American hardwood offering by utilizing extremely selective grading.</p>
        <a href="#">Learn More</a>
      </aside>
    </div>
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
  background: transparent url("../assets/section1.jpg") 50% 50% / cover no-repeat;
  @media only screen and (min-width: 960px) {
    background-image: url("../assets/section1@2x.jpg");
  }
  .article-container {
    @extend %container-width;
    display: grid;
    grid-gap: 20px;
    grid-template-rows: 300px 1fr;
    justify-content: center;
    @media only screen and (min-width: 960px) {
      grid-template-columns: repeat(2, 1fr);
      grid-template-rows: 1fr;
    }
    padding: 80px 0;
    h2 {
      @extend %primary-headline;
      line-height: 2.5;
    }
    p {
      @extend %lead-text;
      max-width: 50ch;
    }
    picture {
      width: 100%;
      justify-self: center;
      @media only screen and (min-width: 960px) {
        width: auto;
        justify-self: end;
      }
      img {
        width: 100%;
        height: auto;
        @media only screen and (min-width: 960px) {
          max-width: 500px;
        }
      }
    }
  }
  .aside-bg {
    background-color: $gray-darker;
    .aside-container {
      @extend %container-width;
      display: grid;
      grid-gap: 80px;
      padding: 80px 0;
      text-align: center;
      justify-content: center;
      @media only screen and (min-width: 960px) {
        grid-template-columns: repeat(3, 1fr);
        grid-gap: 40px;
      }
      aside {
        @media only screen and (min-width: 960px) {
          &:first-child{
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
        color: $tussock;
        text-transform: uppercase;
        font-size: 14px;
        @media only screen and (min-width: 960px) {
          padding-bottom: 20px;
        }
      }
      h4 {
        max-width: 33ch;
      }
      p {
        @extend %paragraph-text;
        color: $gray;
        max-width: 33ch;
        padding: 10px 0;
        @media only screen and (min-width: 960px) {
          padding: 30px 0;
        }
      }
      a {
        @extend %learn-more-link;
      }
    }
  }
}
</style>
