<template>
  <section>
    <div class="section__card">
      <img :src="cardInfo.img" alt="" :class="{imgPosts: posts}" />
      <h3>
        {{ cardInfo.title }}
      </h3>
      <p>{{ cardInfo.text }}</p>
    </div>
  </section>
</template>

<script>
export default {
  name: "AvadaProBarbers",
  props: {
    cardInfo: Object,
  },
};
</script>

<style lang="scss" scoped>
.section__card {
  padding: 0 3rem;
  img {
    height: 110px;
  }
  .imgPosts {
    height: 200px;
  }
}
</style>