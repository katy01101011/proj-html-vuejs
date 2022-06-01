<template>
  <section>
    <div class="shop container">
      <div class="shop__text">
        <h1>Barber Shop</h1>
        <h3>The Pinnacle of Male Grooming</h3>
        <button>Learn More</button>
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
  color: white;
      overflow: hidden;

  .shop {
    height: calc(100vh - $header-height);
    display: flex;
    justify-content: space-between;
    position: relative;
    transform: translateY(-20vh);
    position: relative;

    &__text {
      width: 100%;
        padding-top: $header-height;

      position: relative;
      top: 30vh;

      background-image: url(../assets/avadabarbers_hero_focalmirror.png);
      background-size: 40%;
      background-repeat: no-repeat;
      background-position: right;

      h1 {
        font-family: "Abril Fatface", cursive;
        font-weight: 100;
        font-size: 5.6rem;
        color: $ebb-light-gray;
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
    }
  }
}
</style>