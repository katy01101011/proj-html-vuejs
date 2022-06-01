<template>
  <section>
    <div class="container">
      <h4>Mens grooming</h4>
      <h2>Services</h2>
      <div class="cards" v-if="servicesCards">
        <AvadaSectionCard v-for="(card, index) in servicesCards" :key="index" :cardInfo="card"/>
      </div>
      <div class="cards" v-if="postsCards">
        <AvadaSectionCard v-for="(card, index) in postsCards" :key="'abc' + index" :cardInfo="card"/>
      </div>
      <button>Read about our blog</button>
    </div>
  </section>
</template>

<script>
import AvadaSectionCard from "../components/AvadaSectionCard.vue";

export default {
  name: "AvadaSection",
  components: {
    AvadaSectionCard,
  },
  props: {
    servicesCards: Array, 
    postsCards: Array,
  },
  created() {
    console.log(this.servicesCards, this.postsCards);
  }
};
</script>

<style lang="scss" scoped>
section {
  width: 100%;
  padding: 5rem 0;
  text-align: center;

  .cards {
    width: 100%;
    display: flex;
    justify-content: space-between;
  }
}
</style>