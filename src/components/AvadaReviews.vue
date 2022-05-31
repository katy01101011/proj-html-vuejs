<template>
  <section>
    <h4>subtitle</h4>
    <h2>Reviews</h2>
    <div class="reviews">
      <AvadaReviewsCard />
      <AvadaReviewsCard />
      <AvadaReviewsCard />
    </div>
  </section>
</template>

<script>
import AvadaReviewsCard from "../components/AvadaReviewsCard.vue";

export default {
  name: "AvadaReviews",
  components: {
    AvadaReviewsCard,
  },
};
</script>

<style lang="scss" scoped>
section {
  width: 100%;

  .reviews {
    display: flex;
    justify-content: space-between;
    width: 100%;
  }
}
</style>