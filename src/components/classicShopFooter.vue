<template>
  <footer>
    <div class="top-footer">
      <div class="container">
        <div class="shop-info">
          <img src="../assets/img/classic_shop_logo_footer.png" alt="" />
          <div class="contacts">
            <h6>12345 North Main Street,</h6>
            <h6>New York, NY 555555</h6>
            <h6>Phone: 1.800.555.6789</h6>
            <h6>Email: info@company.com</h6>
            <h6>Web: Theme-Fusion.com</h6>
          </div>
          <div class="social">F T I Y</div>
        </div>
        <div class="top">
          <h5>Top rated products</h5>
          <div v-for="item in topRated" :key="item.name" class="row">
            <div class="item-data">
              <h6>{{ item.name }}</h6>
              <h6>{{ item.rating }}</h6>
              <h6 v-if="item.salePrice != null">
                <span class="overline">${{ item.price }}</span
                ><span class="underline"> ${{ item.salePrice }}</span>
              </h6>
              <h6 v-else>${{ item.price }}</h6>
            </div>
            <div class="item-image">
              <img :src="getImgUrl(item.img)" alt="item.img" />
            </div>
          </div>
        </div>
        <div class="recent">
          <h5>Recent Posts</h5>
          <div class="posts">
            <h6 v-for="post in posts" :key="post">> {{ post }}</h6>
          </div>
        </div>
        <div class="tags">
          <h5>Tags</h5>
          <div class="tag-list">
            <div v-for="tag in tags" :key="tag" class="tag">{{ tag }}</div>
          </div>
        </div>
      </div>
    </div>
    <div class="bottom-footer">
      <h6>&copy; Copyright 2012 - 2020 | Avada Theme by Theme Fusion | All Rights Reserved | Powered by WordPress</h6>
      <img src="../assets/img/payment_cards_footer.png" alt="">
    </div>
  </footer>
</template>

<script>
export default {
  name: "classicShopFooter",
  data() {
    return {
      topRated: [
        {
          name: "Leather Gloves",
          rating: 5,
          price: 45,
          salePrice: null,
          img: "leather_gloves",
        },
        {
          name: "Black Leather Jacket",
          rating: 5,
          price: 235,
          salePrice: 200,
          img: "black_elegant_leather_jacket",
        },
        {
          name: "Spring Printed Dress",
          rating: 5,
          price: 47,
          salePrice: null,
          img: "spring_printed_dress",
        },
      ],
      posts: [
        "Aenean lobortis sapien enim viverra",
        "Duis ac massa sempre maximus",
        "Nunc fermint nulla eu justo sem id",
        "Aliquam posuere magna eget nibh",
        "Cras ac nulla ac consecte rutrum",
        "Fusce mattis nunc ut aliquam",
      ],
      tags: [
        "Black",
        "boots",
        "Brown",
        "Casual",
        "D&G",
        "Fabric",
        "flowers",
        "Grey",
        "hat",
        "Hipster",
        "lines",
        "multi-purpose",
        "New York",
        "Outdoors",
        "red",
        "responsive",
        "summer",
        "sweater",
        "Travel",
        "Warm",
        "White",
        "winter",
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
.top-footer {
  height: 400px;
  background-color: #2b2e32;
  color: $edward;
  display: flex;
  align-items: center;
}
.container {
  display: flex;
  justify-content: space-between;
}
.shop-info {
  img {
    width: 50%;
  }
}
.shop-info,
.top,
.recent,
.tags {
  width: 24%;
  h5 {
    margin-bottom: 2rem;
    text-transform: uppercase;
    font-weight: 500;
  }
}
.contacts {
  margin: 3rem 0;
  h6 {
    margin: 0.5rem 0;
  }
}
.row {
  width: 100%;
  display: flex;
  border-bottom: 0.1px solid $nevada;
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
.posts {
  height: 100%;
  display: flex;
  flex-direction: column;
  h6 {
    border-bottom: 0.1px solid $nevada;
    padding-bottom: 0.7rem;
    margin-bottom: 0.7rem;
  }
}
.tag-list {
  display: flex;
  flex-wrap: wrap;
  .tag {
    margin: 2px;
    padding: 0.7em;
    border: 1px solid $nevada;
    font-size: 10px;
  }
}
.overline {
  text-decoration: line-through;
}
.underline {
  text-decoration: underline;
}
.bottom-footer {
  height: 120px;
  background-color: #1d1f22;
  padding-top: 2rem;
  text-align: center;
  color: $edward;
  img {
    margin-top: 1.5rem;
  }
}
</style>