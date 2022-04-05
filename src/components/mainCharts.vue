<template>
  <div id="charts" class="container">
    <div class="column">
      <h3>featured</h3>
      <div v-for="item in featured" :key="item.article" class="row">
        <div class="item-data">
          <h6>{{ item.article }}</h6>
          <h6 v-if="item.rate != null">{{ item.rate }}</h6>
          <h6 v-if="item.sale != null">
            <span class="overline">{{ item.price }}</span
            ><span class="underline"> {{ item.sale }}</span>
          </h6>
          <h6 v-else>{{ item.price }}</h6>
        </div>
        <div class="item-image">
          <img :src="getImgUrl(item.img)" alt="item.img" />
        </div>
      </div>
    </div>
    <div class="column">
      <h3>on sale</h3>
      <div v-for="item in onSale" :key="item.article" class="row">
        <div class="item-data">
          <h6>{{ item.article }}</h6>
          <h6 v-if="item.rate != null">{{ item.rate }}</h6>
          <h6 v-if="item.sale != null">
            <span class="overline">{{ item.price }}</span
            ><span class="underline"> {{ item.sale }}</span>
          </h6>
          <h6 v-else>{{ item.price }}</h6>
        </div>
        <div class="item-image">
          <img :src="getImgUrl(item.img)" alt="item.img" />
        </div>
      </div>
    </div>
    <div class="column">
      <h3>top rated</h3>
      <div v-for="item in topRated" :key="item.article" class="row">
        <div class="item-data">
          <h6>{{ item.article }}</h6>
          <h6 v-if="item.rate != null">{{ item.rate }}</h6>
          <h6 v-if="item.sale != null">
            <span class="overline">{{ item.price }}</span
            ><span class="underline"> {{ item.sale }}</span>
          </h6>
          <h6 v-else>{{ item.price }}</h6>
        </div>
        <div class="item-image">
          <img :src="getImgUrl(item.img)" alt="item.img" />
        </div>
      </div>
    </div>
    <div class="column">
      <h3>latest reviews</h3>
      <div v-for="item in latestReview" :key="item.article" class="row">
        <div class="item-data">
          <h6>{{ item.article }}</h6>
          <h6 v-if="item.rate != null">{{ item.rate }}</h6>
          <h6 v-if="item.sale != null">
            <span class="overline">{{ item.price }}</span
            ><span class="underline"> {{ item.sale }}</span>
          </h6>
          <h6 v-else>{{ item.price }}</h6>
        </div>
        <div class="item-image">
          <img :src="getImgUrl(item.img)" alt="item.img" />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "mainCharts",
  data() {
    return {
      featured: [
        {
          article: "Black Jacket",
          rate: null,
          price: "$125",
          sale: null,
          img: "black_elegant_leather_jacket",
        },
        {
          article: "Black Leather Jacket",
          rate: 5,
          price: "$235",
          sale: "$200",
          img: "black_elegant_leather_jacket",
        },
        {
          article: "Hipster Black Top",
          rate: null,
          price: "$57",
          sale: null,
          img: "black_elegant_leather_jacket",
        },
      ],
      onSale: [
        {
          article: "Black Leather Jacket",
          rate: 5,
          price: "$125",
          sale: null,
          img: "black_elegant_leather_jacket",
        },
        {
          article: "Blue Leather Jacket",
          rate: 5,
          price: "$235",
          sale: "$200",
          img: "black_elegant_leather_jacket",
        },
        {
          article: "Hipster Black Top",
          rate: null,
          price: "$57",
          sale: null,
          img: "black_elegant_leather_jacket",
        },
      ],
      topRated: [
        {
          article: "Black Jacket",
          rate: null,
          price: "$125",
          sale: null,
          img: "black_elegant_leather_jacket",
        },
        {
          article: "Black Leather Jacket",
          rate: 5,
          price: "$235",
          sale: "$200",
          img: "black_elegant_leather_jacket",
        },
        {
          article: "Hipster Black Top",
          rate: null,
          price: "$57",
          sale: null,
          img: "black_elegant_leather_jacket",
        },
      ],
      latestReview: [
        {
          article: "Black Jacket",
          rate: null,
          price: "$125",
          sale: null,
          img: "black_elegant_leather_jacket",
        },
        {
          article: "Black Leather Jacket",
          rate: 5,
          price: "$235",
          sale: "$200",
          img: "black_elegant_leather_jacket",
        },
        {
          article: "Hipster Black Top",
          rate: null,
          price: "$57",
          sale: null,
          img: "black_elegant_leather_jacket",
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
#charts {
  display: flex;
  .column {
    width: 25%;
  }
}
.row {
  width: 100%;
  display: flex;
  padding-bottom: 0.5rem;
  margin-bottom: 0.5rem;
  .item-data {
    width: 75%;
    display: flex;
    flex-direction: column;
    justify-content: space-evenly;
  }
  .item-image {
    width: 20%;
    img {
      width: 100%;
    }
  }
}
.overline {
  text-decoration: line-through;
}
.underline {
  text-decoration: underline;
}
</style>