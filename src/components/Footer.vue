<template>
  <footer class="footer">
    <section class="footer-links">
      <p>logo</p>
      <ul>
        <li>Who's It For?</li>
        <li>Zen Masters</li>
        <li>Cool People</li>
        <li>Craftsman</li>
      </ul>
      <ul>
        <li>About Us</li>
        <li>About Us</li>
        <li>Pricing</li>
        <li>Customers</li>
      </ul>
      <ul>
        <li>Resources</li>
        <li>Blog</li>
        <li>Case Studies</li>
      </ul>
      <div>
        <p>131 S Dearborn St., Ste 1000<br>
        Chicago, IL 60603</p>
        <p>1.866.878.3231</p>
        <ul>
          <li>twit</li>
          <li>linkd</li>
          <li>face</li>
        </ul>
      </div>
    </section>
    <p class="copyright">&copy; Copyright 2018 Sprout Social, Inc. All Rights Reserved.</p>
  </footer>
</template>

<script>
export default {
  name: "Footer"
};
</script>

<style scoped lang="scss">
@import "../scss/_global";

.footer {
  background-color: $black;
  display: flex;
  color: #fff;
}
</style>
