<template>
  <div id="review">
    <div class="container">
      <img src="../assets/img/man_testimonial.png" alt="">
      <p>Curabitur non tristique tortor. Vestibulum aliquet suscipit ipsum in volutpat. Donec vel lacinia sem, vitae semper nulla. In hac habitasse platea dictumst. Mauris consectetur est et nibh sadip hendrerit bibendum.</p>
      <h4>Darío Pineda, <span class="thin">Theme Fusion</span></h4>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
#review {
  width: 100%;
  height: 600px;
  background-image: url("../assets/img/testimonials_home_1_bg.jpg");
  color: white;
}
.container {
  height: 100%;
  display: flex;
  flex-direction: column;
  justify-content:center;
  align-items: center;
  p {
    margin: 2rem 3rem;
    line-height: 2em;
    font-style: italic;
  }
}
img {
  width: 100px;
}
.thin {
  font-weight: 100;
  margin: 0;
}
</style>