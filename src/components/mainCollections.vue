<template>
  <div id="main-collections">
    <collection-card
      v-for="card in cards"
      :key="card.title"
      :title="card.title"
      :description="card.description"
      :link="card.link"
      :background-img="getImgUrl(card.img)"
    />
  </div>
</template>

<script>
import CollectionCard from "./collectionCard.vue";
export default {
  name: "mainCollections",
  components: {
    CollectionCard,
  },
  data() {
    return {
      cards: [
        {
          title: "Winter Collection",
          description: "Stylish and warm",
          link: "#!",
          img: "winter_collection_bg",
        },
        {
          title: "Spring Collection",
          description: "Bright and colorful",
          link: "#!",
          img: "spring_collection_bg",
        },
        {
          title: "Autumn Collection",
          description: "Rich and comfortable",
          link: "#!",
          img: "autumn_collection_bg",
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

<style>
#main-collections {
  height: 600px;
  display: flex;
}
</style>