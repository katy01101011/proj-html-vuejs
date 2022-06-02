<template>
  <div class="container">
    <section>
      <h4>What people say</h4>
      <h2>Reviews</h2>
      <div class="reviews">
        <AvadaReviewsCard
          v-for="(review, index) in reviews"
          :key="index"
          :card="reviews[index]"
        />
      </div>
    </section>
  </div>
</template>

<script>
import AvadaReviewsCard from "../components/AvadaReviewsCard.vue";
export default {
  name: "AvadaReviews",
  components: {
    AvadaReviewsCard,
  },
  data() {
    return {
      reviews: [
        {
          text: "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Morbi mollis eleifend ante ut sagittis. Sed sodales, urna et imperdiet placerat, ex nisi aliquam orci, ac varius odio libero et arcu.",
          img: require("../assets/avadabarbers-trimcut-gallery6-200x200.jpg"),
          name: "John Doe",
        },
        {
          text: "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Morbi mollis eleifend ante ut sagittis. Sed sodales, urna et imperdiet placerat, ex nisi aliquam orci, ac varius odio libero et arcu.",
          img: require("../assets/avadabarbers-trimcut-gallery7-200x201.jpg"),
          name: "Pete Jones",
        },
        {
          text: "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Morbi mollis eleifend ante ut sagittis. Sed sodales, urna et imperdiet placerat, ex nisi aliquam orci, ac varius odio libero et arcu.",
          img: require("../assets/avadabarbers-trimcut-gallery3-200x201.jpg"),
          name: "Mark Wilson",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
section {
  width: 100%;
  text-align: center;
  padding: 6rem 0;
  h2 {
    margin-bottom: 3rem;
  }
  .reviews {
    display: flex;
    justify-content: space-between;
    width: 100%;
  }
}
</style>