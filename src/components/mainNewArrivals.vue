<template>
  <div id="new-arrivals">
    <h1>New Arrivals</h1>
    <h2>Brand new product form top designers</h2>
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
  name: "mainNewArrivals",
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
@import "../assets/styles/partials/variables";
#new-arrivals {
  margin: 5rem auto;
  text-align: center;
}
h1 {
  &::before,
  &::after {
    content: "";
    display: inline-block;
    height: 2px;
    width: 200px;
    margin: 0 2rem;
    background-color: #f4f4f4;
    vertical-align: middle;
  }
}
h2 {
  color: $nevada;
  font-size: 14px;
  font-weight: 500;
  margin: 1rem 0 3rem 0;
}
.slide-show {
  img {
    width: calc(100% / 5);
  }
}
</style>