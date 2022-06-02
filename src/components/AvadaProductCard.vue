
<template>
  <div>
      <img :src="product.img" alt="">
      <h3>
          {{ product.name }}
      </h3>
      <span>
          {{ product.price }}
      </span>
  </div>
</template>

<script>
export default {
    name: "AvadaProductCard",
    props: {
        product: Object,
    }
}
</script>

<style lang="scss" scoped>
img {
    width: 270px;
}
h3 {
    margin: 1.5rem 0 0 0;
}
</style>