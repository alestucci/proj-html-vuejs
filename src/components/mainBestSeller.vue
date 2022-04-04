<template>
  <div id="best-seller" class="container">
    <h1>Best Seller</h1>
    <h2>Must have products from our top sellers</h2>
    <div class="slide-show">
      <img
        v-for="product in products"
        :key="product.id"
        :src="getImgUrl(product.img)"
        :alt="product.img"
      />
    </div>
  </div>
</template>

<script>
export default {
  name: "mainBestSeller",
  data() {
    return {
      products: [
        {
          id: 1,
          img: "spring_printed_dress",
        },
        {
          id: 2,
          img: "modern_love_tee",
        },
        {
          id: 3,
          img: "black_leather_jacket",
        },
        {
          id: 4,
          img: "black_elegant_leather_jacket",
        },
        {
          id: 5,
          img: "hipster_black_top",
        },
      ],
    };
  },
  methods: {
    getImgUrl(pic) {
      return require("../assets/img/" + pic + ".jpg");
    },
  },
};
</script>

<style lang="scss" scoped>
#best-seller {
  text-align: center;
}
.slide-show {
  img {
    width: calc(100% / 5);
  }
}
</style>