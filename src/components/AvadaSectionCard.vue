<template>
  <section>
    <div class="section__card" :class="{ pad: abc }">
      <div class="img-container" :class="{ big: abc }">
        <img
          :src="cardInfo.img"
          alt=""
          :class="{ imgPosts: posts, bigImg: abc }"
        />
      </div>
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
    abc: Boolean,
  },
};
</script>

<style lang="scss" scoped>
.section__card {
  padding: 0 3rem;

  .img-container {
    img {
      height: 110px;
    }

    .imgPosts {
      height: 200px;
    }
  }

  .big {
    width: 85%;
    height: auto;
    overflow: hidden;
margin: 0 auto;

    .bigImg {
      width: 100%;
      height: auto;
      transition: 1.5s;
    }

    .bigImg:hover {
      transform: scale(120%);
      opacity: 0.9;
      transition: 1.5s;
    }
  }
}

.pad {
  padding: 0 0.5rem;
}
</style>