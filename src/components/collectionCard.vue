<template>
  <div class="card">
    <h1>Winter Collection</h1>
    <h2>Stilish and Warm</h2>
    <div class="btn">View More</div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
.card {
  width: calc(100% / 3);
  height: 100%;
  padding: 2rem 0;
  background-image: url("../assets/img/winter_collection_bg.jpg");
  background-position: top;
  background-size: cover;
  background-repeat: no-repeat;
  text-align: center;
  color: white;
  display: flex;
  flex-direction: column;
  justify-content: flex-end;
}
</style>