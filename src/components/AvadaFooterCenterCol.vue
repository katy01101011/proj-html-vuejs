<template>
  <div class="centerCol">
    <img src="../assets/avadabarbers-logo-x1.png" alt="" />
    <span v-for="(text, index) in centerData.info" :key="index">
      {{ text }}
    </span>
    <div class="icons">
        <h6>Follow us</h6>
      <a v-for="(icon, i) in centerData.social" :key="i">
        <i class="fab" :class="icon"></i>
      </a>
    </div>
  </div>
</template>

<script>
export default {
  name: "AvadaFooterCenterCol",
  props: {
    centerData: Object,
  },
};
</script>

<style lang="scss" scoped>
@import "../style/variables";

.centerCol {
  display: flex;
  flex-direction: column;
  align-items: center;

  img {
    width: 200px;
    margin: 4rem 0 2rem;
  }

  span {
    color: $text-details;
    font-size: 1rem;
    line-height: 0.8rem;
  }

  .icons {
      margin: 1rem;
      text-align: center;
      margin-bottom: 4rem;

      a {
          padding: .3rem;
          margin: .3rem;
          color: $text-details;
          font-size: 1.1rem;
      }
  }

  h6 {
      margin: 2.5rem 0 2rem;
  }
}
</style>