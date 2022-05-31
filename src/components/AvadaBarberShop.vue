<template>
  <section>
    <div class="shop container">
      <div class="shop__text">
        <h1>Barber Shop</h1>
        <h3>The Pinnacle of Male Grooming</h3>
        <button>Learn More</button>
      </div>
      <div class="shop__image">
        <img src="../assets/avadabarbers_hero_focalmirror.png" alt="" />
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "AvadaBarberShop",
};
</script>

<style lang="scss" scoped>
@import "../style/variables";

section {
  height: 100vh;
  background-image: url(../assets/avadabarbers-homepage-hero-bg.jpg);
  background-size: cover;
  background-repeat: no-repeat;
  padding-top: $header-height;
  color: white;

  .shop {
    height: calc(100vh - $header-height);
    display: flex;
    justify-content: space-between;
    position: relative;
    transform: translateY(-20vh);

    &__text {
      position: relative;
      top: 30vh;

      h1 {
        font-family: "Abril Fatface", cursive;
        font-weight: 100;
        font-size: 5.6rem;
      }

      h1::after {
        content: "";
        display: block;
        margin-top: 1rem;
        margin-bottom: 2.5rem;
        width: 250px;
        height: 4.5px;
        background-color: $text-secondary;
      }

      h3 {
        font-size: 1.5rem;
        color: $text-details;
        margin-bottom: 2.5rem;
      }

      button {
        background-color: transparent;
        border: 2px solid $text-secondary;
        color: $text-secondary;
        text-transform: uppercase;
        font-size: 1.2rem;
        padding: 1rem 2.4rem;
      }
    }

    &__image {
      margin-top: 1rem;
      width: 38vw;
    }
  }
}
</style>