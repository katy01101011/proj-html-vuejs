<template>
  <div id="app">
    <AvadaHeader />
    <main>
      <AvadaBarberShop />
      <AvadaProBarbers />
      <div id="triangleUp"></div>
      <AvadaSection :servicesCards="services" />
      <div id="triangleUpBlack"></div>
      <AvadaProducts />
      <AvadaMonthsProduct />
      <AvadaReviews />
      <div id="triangleDown"></div>
      <AvadaSection :postsCards="posts" style="background-color: #eae8e6" />
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
        },
      ],
      services: [
        {
          img: require("./assets/avadabarbers-trimcut-icon-before.png"),
          title: "Trim & Cut",
          text: "Avada Barbers are experts in the lickety split trim and hair cut. Quick but careful and ridiculously good looking.",
        },
        {
          img: require("./assets/avadabarbers-washndry-icon.png"),
          title: "Wash & Dry",
          text: "Take a seat in our fine leather chairs, lean back and let us lather you a fresh head in a luxurious fashion.",
        },
        {
          img: require("./assets/avadabarbers-beardtrim-icon.png"),
          title: "Beard Tidy",
          text: "Tame the tangles and untidy facial hairs like a gentleman with our Beard Tidy services from Avada Barbers.",
        },
      ],
      posts: [
        {
          img: require("./assets/avadabarbers-second-blog-320x202.jpg"),
          title: "Avada Barbers Now Open",
          text: "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Phasellus ut dapibus magna. Praesent semper,",
        },
        {
          img: require("./assets/avadabarbers-choosing-blog-320x202.jpg"),
          title: "Choosing The Right Barber",
          text: "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Phasellus ut dapibus magna. Praesent semper,",
        },
        {
          img: require("./assets/avadabarbers-ourservice-blog-320x202.jpg"),
          title: "Quick Service Guide",
          text: "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Phasellus ut dapibus magna. Praesent semper,",
        },
      ],
    };
  },
};
</script>

<style lang="scss">
@import "./style/general.scss";
@import "./style/variables";
@import "./style/mixins.scss";
@import "~@fortawesome/fontawesome-free/css/all.min.css";

#app {
  // font-family: "Abril Fatface", cursive;

  main {
    width: 100%;
    color: $text-primary;
  }

  #triangleUp {
    width: 0;
    height: 0;
    border-left: 50vw solid $cod-gray-light-black;
    border-right: 50vw solid $cod-gray-light-black;
    border-bottom: 110px solid white;
  }

    #triangleUpBlack {
    width: 0;
    height: 0;
    border-left: 50vw solid transparent;
    border-right: 50vw solid transparent;
    border-bottom: 110px solid $cod-gray-light-black;
    margin-top: 5rem
  }

  #triangleDown {
      width: 0;
      height: 0;
      border-left: 50vw solid $ebb-light-gray;
      border-right: 50vw solid $ebb-light-gray;
      border-top: 110px solid white;
      padding-bottom: 2rem;
    }
}
</style>
