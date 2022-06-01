<template>
  <section>
    <div class="container">
      <h4>We have you covered</h4>
      <h2>Avada Grooming Products</h2>
      <div class="products">
        <AvadaProductCard
          v-for="(product, index) in products"
          :key="index"
          :product="product"
        />
      </div>
      <button>Shop our product range</button>
    </div>
  </section>
</template>

<script>
import AvadaProductCard from "./AvadaProductCard.vue";
export default {
  name: "AvadaProducts",
  components: {
    AvadaProductCard,
  },
  data() {
    return {
      products: [
        {
          img: require("../assets/brush_dark-400x400.png"),
          name: "Brush",
          price: "$15.00",
        },
        {
          img: require("../assets/scissors-200x200.png"),
          name: "Scissors",
          price: "$85.00",
        },
        {
          img: require("../assets/hot_oil_dark-200x200.png"),
          name: "Hot Oil",
          price: "$15.00",
        },
        {
          img: require("../assets/straight_razor_dark-200x200.png"),
          name: "Straight Razor",
          price: "$30.00",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
section {
  background-image: url(../assets/avadabarbers-reviewsbackground.jpg);
  background-position: start;
  background-size: cover;
  background-repeat: no-repeat;
  text-align: center;
  padding: 6rem 0;

  .container {
    width: 84%;

    h2 {
      margin-bottom: 3rem;
    }

    .products {
      display: flex;
      justify-content: space-between;
    }

    button {
        margin-top: 5rem;
        margin-bottom: 5rem;
    }
  }
}
</style>