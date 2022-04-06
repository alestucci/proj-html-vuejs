<template>
  <div id="card">
    <img :src="productImg" alt="productName" />
    <h1 id="item-name">{{ productName }}</h1>
    <h2 id="tags">{{ productTags }}</h2>
    <h3 v-if="productSale != null">
      <span class="prev-price">${{
        productPrice
      }}</span> $
      {{ productSale }}
    </h3>
    <h3 v-else>${{ productPrice }}</h3>
  </div>
</template>

<script>
export default {
  name: "featuredCard",
  props: {
    productName: String,
    productTags: String,
    productPrice: Number,
    productSale: null,
    productImg: String,
  },
};
</script>

<style lang="scss" scoped>
@import "../assets/styles/partials/variables";
#card {
  text-align: left;
  width: calc(100% / 4);
}
img {
  width: 100%;
}
h1 {
  font-size: 14px;
}
h2 {
  font-size: 12px;
  font-weight: 300;
  color: $nevada;
  margin: .4rem 0;
}
h3 {
  font-size: 12px;
  font-weight: 300;
  color: $havelock-blue;
  margin: .4rem 0;
}
.prev-price {
  text-decoration: line-through;
}
</style>