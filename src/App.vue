<template>
  <div id="app">
    <AvadaHeader />
    <main>
      <AvadaBarberShop />
      <AvadaProBarbers />
      <AvadaSection />
      <AvadaProducts />
      <AvadaMonthsProduct />
      <AvadaReviews />
      <AvadaSection />
      <AvadaSection />
    </main>
    <AvadaFooter />
  </div>
</template>

<script>
import AvadaHeader from "./components/AvadaHeader.vue";
import AvadaBarberShop from "./components/AvadaBarberShop.vue";
import AvadaProBarbers from "./components/AvadaProBarbers.vue";
import AvadaSection from "./components/AvadaSection.vue";
import AvadaProducts from "./components/AvadaProducts.vue";
import AvadaMonthsProduct from "./components/AvadaMonthsProduct.vue";
import AvadaReviews from "./components/AvadaReviews.vue";
import AvadaFooter from "./components/AvadaFooter.vue";
import "@fontsource/abril-fatface";
import "@fontsource/lato";

export default {
  name: "App",
  components: {
    AvadaHeader,
    AvadaBarberShop,
    AvadaProBarbers,
    AvadaSection,
    AvadaProducts,
    AvadaMonthsProduct,
    AvadaReviews,
    AvadaFooter,
  },
  data() {
    return {
      menuIcons: [
        {
          name: "Shopping Cart",
          icon: "shopping-cart",
        },
        {
          name: "menu",
          icon: "bars",
        }
      ],
    }
  },
};
</script>

<style lang="scss">
@import "./style/general.scss";
@import "./style/variables";
@import "./style/mixins.scss";
@import "~@fortawesome/fontawesome-free/css/all.min.css";

#app {
  * {
    // font-family: "Abril Fatface", cursive;
    // border: 1px solid black;
  }

  main {
    width: 100%;
    height: 10000px;
    color: $text-primary;
    background-color: orange;
  }

  p {
    font-family: "Lato", sans-serif;
  }
}
</style>
