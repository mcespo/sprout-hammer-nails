<template>
  <footer class="footer">
    <HammerNailsLogo class="footer-logo" />
    <section class="footer-links">
      <ul>
        <li>Who's It For?</li>
        <li><a href="#">Zen Masters</a></li>
        <li><a href="#">Cool People</a></li>
        <li><a href="#">Craftsman</a></li>
      </ul>
      <ul>
        <li>About Us</li>
        <li><a href="#">About Us</a></li>
        <li><a href="#">Pricing</a></li>
        <li><a href="#">Customers</a></li>
      </ul>
      <ul>
        <li>Resources</li>
        <li><a href="#">Blog</a></li>
        <li><a href="#">Case Studies</a></li>
      </ul>
      <div class="address">
        <p>131 S Dearborn St., Ste 1000 Chicago, IL 60603</p>
        <p>1.866.878.3231</p>
        <ul class="icons">
          <li><a href="#"><img src="../assets/icon_footer-twitter.svg" alt=""></a></li>
          <li><a href="#"><img src="../assets/icon_footer-linkedin.svg" alt=""></a></li>
          <li><a href="#"><img src="../assets/icon_footer-facebook.svg" alt=""></a></li>
        </ul>
      </div>
    </section>
    <p class="copyright">&copy; Copyright 2018 Sprout Social, Inc. All Rights Reserved.</p>
  </footer>
</template>

<script>
import HammerNailsLogo from "./icons/HammerNailsLogo.vue";
export default {
  name: "Footer",
  components: {
    HammerNailsLogo
  }
};
</script>

<style scoped lang="scss">
@import "../scss/_global";

.footer {
  @extend %container-width;
  background-color: $black;
  display: grid;
  color: $white;
  padding: 80px 0 200px;
  justify-content: center;
  text-align: center;
  @media only screen and (min-width: 960px) {
    text-align: left;
    grid-auto-rows: auto;
    grid-template-columns: 350px 1fr;
  }
  ul {
    list-style: none;
  }
  .footer-logo {
    justify-self: center;
    width: 220px;
    padding-bottom: 40px;
    @media only screen and (min-width: 960px) {
      justify-self: left;
      grid-row: 1/2;
    }
  }
  .footer-links {
    font-size: 13px;
    justify-self: center;
    display: grid;
    grid-gap: 40px;
    grid-column: 1/2;
    @media only screen and (min-width: 960px) {
      grid-template-columns: repeat(4, 1fr);
      grid-column: 2/3;
    }
    .address {
      width: 15ch;
      p:nth-child(2) {
        padding-top: 8px;
      }
    }
    .icons {
      margin: 20px 0 0 0;
      display: flex;
      flex-flow: row;
      justify-content: space-around;
      @media only screen and (min-width: 960px) {
        justify-content: flex-start;
      }
      img {
        width: 30px;
        @media only screen and (min-width: 960px) {
          margin-right: 20px;
        }
      }
    }
    p {
      font-size: 13px;
    }
    ul {
      font-size: 13px;
      li {
        padding-bottom: 8px;
        font-size: 13px;
        &:first-child {
          font-weight: 700;
          text-transform: uppercase;
        }
        a {
          font-size: 13px;
          color: $tussock;
          text-decoration: none;
          transition: color 300ms ease-in-out;
          &:hover {
            color: saturate($tussock, 40%);
          }
        }
      }
    }
  }
  .copyright {
    color: $tussock;
    padding-top: 80px;
    font-size: 13px;
    text-align: center;
    grid-column: 1/2;
    @media only screen and (min-width: 960px) {
      grid-column: 1/3;
      grid-row: 2/3;
    }
  }
}
</style>
