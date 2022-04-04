<template>
  <div id="slider">
    <h1>Brand New Arrivals</h1>
    <h2>new collection from new york</h2>
    <div>
      <div class="btn">View all</div>
      <div class="btn">Lookbook</div>
    </div>
  </div>
</template>

<script>
export default {
  name: "mainSlider",
};
</script>

<style lang="scss" scoped>
#slider {
  height: 600px;
  font-family: "Montserrat", sans-serif;
  letter-spacing: 0.2em;
  color: white;
  background-image: url(../assets/img/home1_slide_three_bg_2.jpg);
  background-position: center;
  background-size: cover;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
h1 {
  font-size: 60px;
  cursor: pointer;
}
h2 {
  margin: 1rem 0;
  text-transform: uppercase;
  font-size: 20px;
  font-weight: 100;
  cursor: pointer;
}
.btn {
  display: inline-block;
  margin: 1rem 0.5rem;
  font-size: 15px;
  font-weight: 500;
  letter-spacing: 0;
  text-align: center;
  text-transform: uppercase;
  padding: 1rem 2rem;
  border: 1px solid white;
  border-radius: 1.5rem;
  background-color: rgba($color: white, $alpha: 0.1);
  cursor: pointer;
}
</style>