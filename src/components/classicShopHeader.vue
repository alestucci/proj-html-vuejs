<template>
  <header>
    <div class="top-header">
      <div class="container">
      <div class="social">
        <font-awesome-icon icon="fa-brands fa-facebook-f" />
        <font-awesome-icon icon="fa-brands fa-twitter" />
        <font-awesome-icon icon="fa-brands fa-instagram" />
        <font-awesome-icon icon="fa-brands fa-youtube" />
        <font-awesome-icon icon="fa-brands fa-pinterest-p" />
      </div>
      <div class="cart">
        <ul>
          <li>Shopping Cart</li>
          <li>My Account</li>
        </ul>
        <span class="cart-grey"
          ><font-awesome-icon icon="fa-solid fa-cart-shopping" />CART
          <font-awesome-icon icon="fa-solid fa-chevron-down"
        /></span>
      </div>
      </div>
    </div>
    <div class="bottom-header">
      <div class="container">
        <img src="../assets/img/classic_shop_logo2x.png" alt="Logo" />
        <nav>
          <ul>
            <li v-for="link in links" :key="link.text">
              <a :href="link.href"
                >{{ link.text
                }}<font-awesome-icon
                  icon="fa-solid fa-chevron-down"
                  v-if="link.chevron"
              /></a>
            </li>
          </ul>
          <div class="btn">Shop now!</div>
          <div class="search">
            <font-awesome-icon icon="fa-solid fa-magnifying-glass" />
          </div>
        </nav>
      </div>
    </div>
  </header>
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
* {
  font-size: 12px;
}
.container {
  height: 100%;
  display: flex;
  justify-content: space-between;
  align-items: center;
  .social > * {
    margin-right: 1rem;
  }
  img {
    width: 160px;
  }
}
.top-header {
  height: 50px;
  border-bottom: 1px solid #f8f8f8;
  color: #575C61;
}
.bottom-header {
  height: 105px;
  border-bottom: 1px solid #f8f8f8;
  color: #575C61;
  ul {
    height: 100%;
  }
}
.cart ul {
  height: 50px;
  padding: 0;
}
li,
.cart > * {
  display: inline-block;
  padding: 0 1rem;
}
.cart li:nth-child(2) {
  height: 100%;
  border-left: 1px solid #f8f8f8;
  border-right: 1px solid #f8f8f8;
}
.cart-grey {
  height: 50px;
  background-color: #fafafa;
}
nav {
  display: flex;
}
a {
  text-decoration: none;
  color: inherit;
}
.btn{
  padding: .5rem 1rem;
  background-color: #427ED1;
  color: white;
  border-radius: .5rem;
}
.search {
  padding: 0 1rem;
}
</style>