<template>
  <div id="main-collections">
    <collection-card v-for="card in cards" :key="card.title" />
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
        },
        {
          title: "Spring Collection",
          description: "Bright and colorful",
          link: "#!",
        },
        {
          title: "Autumn Collection",
          description: "Rich and comfortable",
          link: "#!",
        },
      ],
    };
  },
};
</script>

<style>
#main-collections {
  height: 600px;
  display: flex;
}
</style>