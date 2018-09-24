<template>
  <header class="header">
    <h1>Bespoke Wood Products?</h1>
    <p>Inventive design coupled with skilled craftsmanship and advanced machinery result in high
quality finished product by mastercraftsman Nate Turner.</p>
    <a class="cta" href="#">Request More Info</a>
  </header>
</template>

<script>
export default {
  name: "Header"
};
</script>

<style scoped lang="scss">
.header {
  background-color: #ccc;
  display: flex;
  flex-direction: column;
  align-items: center;
  text-align: center;
  h1 {
    font-weight: 800;
  }
  .cta {
    width: 180px;
  }
}
</style>
