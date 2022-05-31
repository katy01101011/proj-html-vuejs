<template>
  <section>
    <h4>subtitle</h4>
    <h2>Section Title</h2>
    <div class="cards">
      <AvadaSectionCard />
      <AvadaSectionCard />
      <AvadaSectionCard />
    </div>
    <div>Button</div>
  </section>
</template>

<script>
import AvadaSectionCard from "../components/AvadaSectionCard.vue";

export default {
  name: "AvadaSection",
  components: {
    AvadaSectionCard,
  },
};
</script>

<style lang="scss" scoped>
section {
  width: 100%;
  text-align: center;

  .cards {
    width: 100%;
    display: flex;
    justify-content: space-between;
  }
}
</style>