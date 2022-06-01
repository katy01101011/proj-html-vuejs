<template>
  <section>
    <div class="pro container">
      <h4>Award winning</h4>
      <h2>Pro Barbers</h2>
      <button>Meet your new barber</button>
    </div>
  </section>
</template>

<script>
export default {
  name: "AvadaProBarbers",
};
</script>

<style lang="scss" scoped>
@import "../style/general.scss";
@import "../style/variables";

section {
  background-image: url(../assets/avadabarbers-about-introbackground.jpg);
  background-size: cover;
  background-repeat: no-repeat;

  .pro {
    padding: 6rem 0 16rem;
    text-align: center;

    h2 {
        margin-bottom: 1.5rem;
    }
  }
}
</style>