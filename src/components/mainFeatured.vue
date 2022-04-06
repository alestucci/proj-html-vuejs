<template>
  <div id="featured" class="container">
    <h1>Featured Products</h1>
    <h2>Must have products from our top sellers</h2>
    <div class="menu">
      <ul>
        <li v-for="category in categories" :key="category.name">
          <a :href="category.link">{{ category.name }}</a>
        </li>
      </ul>
    </div>
    <div class="cards">
      <featured-card
        v-for="item in products"
        :key="item.name"
        :product-name="item.name"
        :product-tags="item.tags"
        :product-price="item.price"
        :product-sale="item.salePrice"
        :product-img="getUrlImg(item.img)"
      />
    </div>
  </div>
</template>

<script>
import featuredCard from "./featuredCard.vue";
export default {
  components: { featuredCard },
  name: "mainFeatured",
  data() {
    return {
      activeIndex: 0,
      categories: [
        {
          name: "Men",
          link: "#!",
        },
        {
          name: "Women",
          link: "#!",
        },
        {
          name: "Accessories",
          link: "#!",
        },
      ],
      products: [
        {
          name: "Black Leather Jacket",
          tags: "Men, Jacket, Jeans",
          price: 235,
          salePrice: 200,
          img: "black_elegant_leather_jacket",
        },
        {
          name: "Black Leather Suit",
          tags: "Men, Jacket",
          price: 176,
          salePrice: null,
          img: "black_leather_suit",
        },
        {
          name: "Blue Jacket & Stripe Tee",
          tags: "Men, Jacket, Suits",
          price: 580,
          salePrice: null,
          img: "blue_jacket_and_white_stripe_tee",
        },
        {
          name: "Modern Black Leather Suit",
          tags: "Men, Jacket",
          price: 96,
          salePrice: null,
          img: "modern_black_leather_suit",
        },
      ],
    };
  },
  methods: {
    getUrlImg(img) {
      return require("../assets/img/" + img + ".jpg");
    },
  },
};
</script>

<style lang="scss" scoped>
@import "../assets/styles/partials/variables";
#featured {
  margin: 5rem auto;
  text-align: center;
  overflow: hidden;
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
li {
  display: inline-block;
  font-weight: 600;
  padding: 1rem 3rem;
  border: 1px solid #f3f3f3;
}
a {
  color: inherit;
  text-decoration: none;
}
.cards {
  margin: 3rem 0 6rem;
  display: flex;
  justify-content: center;
}
</style>