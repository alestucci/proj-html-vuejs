<template>
  <div class="container">
    <div class="top-header">
      <div class="social">F T I Y</div>
      <div class="cart">
        <ul>
          <li>Shopping Cart</li>
          <li>My Account</li>
        </ul>
        <span>Cart</span>
      </div>
    </div>
    <div class="bottom-header">
      <img src="../assets/img/classic_shop_logo2x.png" alt="Logo" />
      <nav>
        <ul>
          <li v-for="link in links" :key="link.text"><a :href="link.href">{{ link.text }}</a></li>
        </ul>
        <div class="btn">Shop now!</div>
        <div class="search">C</div>
      </nav>
    </div>
  </div>
</template>

<script>
export default {
  name: "classicShopHeader",
  data() {
    return {
      links: [
        {
          href: "#",
          text: "Home",
          chevron: true,
        },
        {
          href: "#",
          text: "Shop",
          chevron: true,
        },
        {
          href: "#",
          text: "Products",
          chevron: true,
        },
        {
          href: "#",
          text: "Categories",
          chevron: true,
        },
        {
          href: "#",
          text: "News",
          chevron: false,
        },
        {
          href: "#",
          text: "Elements",
          chevron: true,
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
.top-header,
.bottom-header {
  display: flex;
  justify-content: space-between;
  img {
    width: 200px;
  }
}
li,
.cart > * {
  display: inline-block;
  margin: 0 1rem;
}
nav {
  display: flex;
}
a {
  text-decoration: none;
  color: inherit;
}
</style>