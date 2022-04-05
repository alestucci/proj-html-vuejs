<template>
  <div id="charts" class="container">
    <div>
      <h3>featured</h3>
			<chart-row />
			<chart-row />
			<chart-row />
    </div>
    <div>
      <h3>on sale</h3>
			<chart-row />
			<chart-row />
			<chart-row />
    </div>
    <div>
      <h3>top rated</h3>
			<chart-row />
			<chart-row />
			<chart-row />
    </div>
    <div>
      <h3>latest reviews</h3>
			<chart-row />
			<chart-row />
			<chart-row />
    </div>
  </div>
</template>

<script>
import chartRow from './chartRow.vue';
export default {
  components: { chartRow },
  name: "mainCharts",
  data() {
    return {
      featured: [
        {
          article: "Black Jacket",
          rate: null,
          price: "$125",
          sale: null,
        },
        {
          article: "Black Leather Jacket",
          rate: 5,
          price: "$235",
          sale: "$200",
        },
        {
          article: "Hipster Black Top",
          rate: null,
          price: "$57",
          sale: null,
        },
      ],
      onSale: [
        {
          article: "Black Leather Jacket",
          rate: 5,
          price: "$125",
          sale: null,
        },
        {
          article: "Blue Leather Jacket",
          rate: 5,
          price: "$235",
          sale: "$200",
        },
        {
          article: "Hipster Black Top",
          rate: null,
          price: "$57",
          sale: null,
        },
      ],
      topRated: [
        {
          article: "Black Jacket",
          rate: null,
          price: "$125",
          sale: null,
        },
        {
          article: "Black Leather Jacket",
          rate: 5,
          price: "$235",
          sale: "$200",
        },
        {
          article: "Hipster Black Top",
          rate: null,
          price: "$57",
          sale: null,
        },
      ],
      latestReview: [
        {
          article: "Black Jacket",
          rate: null,
          price: "$125",
          sale: null,
        },
        {
          article: "Black Leather Jacket",
          rate: 5,
          price: "$235",
          sale: "$200",
        },
        {
          article: "Hipster Black Top",
          rate: null,
          price: "$57",
          sale: null,
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
#charts {
  display: flex;
  div {
    width: 25%;
  }
}
</style>