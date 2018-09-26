<template>
  <nav>
    <div class="container">
      <HammerNailsLogo class="nav-logo" />
      <ul class="nav-info">
        <li><a href="#">Solutions</a></li>
        <li><a href="#">Pricing</a></li>
        <li><a href="#">About</a></li>
      </ul>
      <ul class="nav-login">
        <li><a href="#">Login</a></li>
        <li><a class="cta" href="#">Start Your Free Trial</a></li>
      </ul>
      <!-- <Slide right id="mobileNav" /> -->
    </div>
  </nav>
</template>

<script>
import HammerNailsLogo from "./icons/HammerNailsLogo.vue";
import { Slide } from 'vue-burger-menu';

export default {
  name: "Navbar",
  components: {
    HammerNailsLogo,
    Slide
  }
};
</script>

<style scoped lang="scss">
@import "../scss/_global";

nav {
  z-index: 2;
  position: fixed;
  width: 100vw;
  height: 72px;
  background-color: $white;

  ul {
    list-style: none;
    @media only screen and (min-width: 960px) {
      display: flex;
    }

    li:not(:last-child) {
      margin-right: 2em;
    }
  }

  a {
    text-decoration: none;
    font-weight: 700;
  }

  .container {
    @extend %container-width;
    height: 100%;
    display: grid;
    align-items: center;
    justify-content: space-between;
    grid-template-columns: repeat(2, 1fr);
    @media only screen and (min-width: 960px) {
      grid-template-columns: repeat(3, 1fr);
    }

    .nav-logo {
      justify-self: start;
      max-width: 180px;
      margin-top: -6px;
      @media only screen and (min-width: 960px) {
        max-width: 220px;
      }
    }

    .nav-info {
      justify-self: center;
       display: none;
      @media only screen and (min-width: 960px) {
        display: flex;
      }
      a {
        color: $gray-dark;
        transition: color 300ms ease-in-out;
        &:hover {
          color: saturate($gray-dark, 40%);
        }
      }
    }

    .nav-login {
      justify-self: end;
      .cta {
        @media only screen and (max-width: 959px) {
          padding: 14px;
          font-size: 14px
        }
      }
      li:first-child a {
        color: $gray;
        transition: color 300ms ease-in-out;
        display: none;
        @media only screen and (min-width: 960px) {
          display: flex;
        }
        &:hover {
          color: saturate($gray, 40%);
        }
      }
    }
  }
}

#mobileNav {
  #sideNav {
    background-color: $gray;
  }
  .bm-burger-button {
    background-color: gold;
  }
}

</style>
