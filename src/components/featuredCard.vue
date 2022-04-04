<template>
  <div id="card">
    <img src="../assets/img/black_elegant_leather_jacket.jpg" alt="" />
    <h1 id="item-name">Black Leather Jacket</h1>
    <h2 id="tags">Men, Jacket, Jeans</h2>
    <h3 id="prev-price">$235</h3>
    <h3 id="price">$200</h3>
  </div>
</template>

<script>
export default {
  name: "featuredCard",
};
</script>

<style lang="scss" scoped>
#card {
  text-align: left;
  width: calc(100% / 4);
}
img {
    width: 100%;
}
h3 {
  display: inline-block;
  margin-right: 0.5rem;
}
</style>