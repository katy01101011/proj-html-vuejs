<template>
    <div class="sideCol">
          <img :src="side.img" alt="">
  <button>
      {{ side.btn }}
  </button>
    </div>
</template>

<script>

export default {
    name: "AvadaFooterSideCol",
    props: {
        side: Object,
    }
}
</script>

<style lang="scss" scoped>
@import "../style/variables";

.sideCol {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;

    img {
        width: 350px;
    }

    button {
        font-size: 1rem;
        margin-top: 2rem;
        padding: .8rem 1.6rem
    }
}
</style>