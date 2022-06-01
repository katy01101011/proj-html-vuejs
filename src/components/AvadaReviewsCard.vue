<template>
  <div class="card">
    <p>
{{ card.text }}
    </p>
<img :src="card.img" alt="">
    <h5>
      {{ card.name }}
    </h5>
  </div>
</template>

<script>
export default {
  name: "AvadaReviewsCard",
  props: {
    card: Object,
  }
};
</script>

<style lang="scss" scoped>
    .card {
        text-align: center;
        padding: 0 3rem;

        img {
          width: 120px;
          border-radius: 50%;
          margin: 1.5rem 0 1rem 0;
        }
    }
</style>