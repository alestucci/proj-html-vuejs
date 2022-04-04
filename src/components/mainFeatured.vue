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
      <featured-card />
      <featured-card />
      <featured-card />
      <featured-card />
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
    };
  },
};
</script>

<style lang="scss" scoped>
#featured {
  text-align: center;
  overflow: hidden;
}
li {
  display: inline-block;
  font-weight: 600;
  padding: 1rem 3rem;
  border: 1px solid black;
}
a {
  color: inherit;
  text-decoration: none;
}
.cards {
  display: flex;
  justify-content: center;
}
</style>