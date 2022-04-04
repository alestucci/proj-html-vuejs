<template>
  <div>
    <main-slider />
    <main-featured />
    <main-collections />
    <main-best-seller />
    <main-promotions />
    <main-new-arrivals />
    <main-review />
    <main-blog />
    <main-charts />
    <main-brands />
    <main-newsletter />
  </div>
</template>

<script>
import mainSlider from "./mainSlider.vue";
import mainFeatured from "./mainFeatured.vue";
import mainCollections from "./mainCollections.vue";
import mainBestSeller from "./mainBestSeller.vue";
import mainPromotions from "./mainPromotions.vue";
import mainNewArrivals from "./mainNewArrivals.vue";
import mainReview from "./mainReview.vue";
import mainBlog from "./mainBlog.vue";
import mainCharts from "./mainCharts.vue";
import mainBrands from "./mainBrands.vue";
import mainNewsletter from "./mainNewsletter.vue";

export default {
  name: "classicShopMain",
  components: {
    mainSlider,
    mainFeatured,
    mainCollections,
    mainBestSeller,
    mainPromotions,
    mainNewArrivals,
    mainReview,
    mainBlog,
    mainCharts,
    mainBrands,
    mainNewsletter,
  },
};
</script>

<style>
</style>