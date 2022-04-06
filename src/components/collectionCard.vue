<template>
  <div
    class="card"
    :style="{ backgroundImage: `url(&quot;${backgroundImg}&quot;)` }"
  >
    <h1>{{ title }}</h1>
    <h2>{{ description }}</h2>
    <div>
      <div class="btn">View More</div>
    </div>
  </div>
</template>

<script>
export default {
  name: "collectionCard",
  props: {
    title: String,
    description: String,
    link: String,
    backgroundImg: String,
  },
};
</script>

<style lang="scss" scoped>
.card {
  width: calc(100% / 3);
  height: 100%;
  padding: 2rem 0;
  background-position: top;
  background-size: cover;
  background-repeat: no-repeat;
  text-align: center;
  color: white;
  display: flex;
  flex-direction: column;
  justify-content: flex-end;
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