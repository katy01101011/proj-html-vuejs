<template>
  <div class="container">
    <section class="product">
      <div class="product__image">
        <img src="../assets/shaving_butter-400x400.png" alt="" />
      </div>
      <div class="product__text">
        <h4>This months featured product</h4>
        <h2>Shaving Butter</h2>
        <p>
          Lorem ipsum dolor sit amet, consectetur adipiscing elit. Pellentesque
          laoreet enim est, vel molestie dolor ultrices ut. Lorem ipsum dolor
          sit amet, consectetur adipiscing elit.
        </p>
        <button>Buy now</button>
      </div>
    </section>
  </div>
</template>

<script>
export default {
  name: "AvadaMonthsProduct",
};
</script>

<style lang="scss" scoped>
@import "../style/variables";

.product {
  background-color: black;
  border-top: 4px solid $teak-brown;
  position: relative;
  bottom: 50px;
  display: flex;
  height: calc(27vw + 4px);

  &__image {
    background-image: url(../assets/avadabarbers-cta-background.jpg);
    background-size: cover;
    background-repeat: no-repeat;
    padding: 2rem;
      max-height: 27vw;
      min-width: 27vw;
      max-height: 27vw;
      min-height: 27vw;
      display: flex;
      justify-content: center;
      align-items: center;

  }

  &__text {
    padding: 3.5rem;
      overflow-y: scroll;

    p {
      padding: 1.5rem 0;
      color: $text-details;
    }
  }
}
</style>