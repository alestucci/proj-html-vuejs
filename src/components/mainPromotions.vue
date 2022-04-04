<template>
  <div id="promotions">
    <div class="container">
      <div class="card sale">
        <h1>70% Off</h1>
        <p>Vivamus tempor leo lacus, feugiat ut magna aliquam erat.</p>
        <div class="btn">View more</div>
      </div>
      <div class="card shipping">
        <h1>Free Shipping</h1>
        <p>Vivamus tempor leo lacus, feugiat ut magna aliquam erat.</p>
        <div class="btn">View more</div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "mainPromotions",
};
</script>

<style lang="scss" scoped>
#promotions {
  height: 400px;
  display: flex;
  align-items: center;
  background-image: url("../assets/img/bkgd_confetti-compressor.jpg");
  background-size: cover;
  background-position: center;
}
.container {
  display: flex;
  justify-content: space-between;
}
.card {
  width: 48%;
  padding: 5rem 7rem 5rem 3rem;
  color: white;
}
.sale {
  background-image: url("../assets/img/promo_box_1_bg.jpg");
  background-size: cover;
}
.shipping {
  background-image: url("../assets/img/promo_box_2_bg.jpg");
  background-size: cover;
}
</style>