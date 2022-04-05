<template>
  <div id="newsletter">
    <div class="container">
      <div id="M">M</div>
      <h2>Subscribe now and get special offers</h2>
      <input type="text" placeholder="Insert your email" />
      <div class="btn-blue">Send</div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
@import "../assets/styles/partials/variables";
#newsletter {
  background-color: $shark-other;
  color: white;
}
.container {
  height: 200px;
  display: flex;
  justify-content: space-between;
  align-items: center;
}
#M {
  height: 4rem;
  width: 4rem;
  background-color: black;
	color: $edward;
  border-radius: 100%;
	display: flex;
  justify-content: center;
  align-items: center;
}
</style>