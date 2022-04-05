<template>
  <div id="brands">
    <div class="container">
      <h4>Brand logos</h4>
      <div class="slides">
        <img src="../assets/img/b_logotype_1.png" alt="" />
        <img src="../assets/img/b_logotype_2.png" alt="" />
        <img src="../assets/img/b_logotype_3.png" alt="" />
        <img src="../assets/img/b_logotype_4.png" alt="" />
        <img src="../assets/img/b_logotype_5.png" alt="" />
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
@import "../assets/styles/partials/variables";
#brands {
  background-color: lightgray;
  height: 300px;
  display: flex;
  align-items: center;
	text-align: center;
}
.slides {
	margin-top: 3rem;
  display: flex;
  justify-content: space-between;
}
img {
  width: 12%;
}
</style>