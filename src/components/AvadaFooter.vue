<template>
  <footer>
    <div class="container">
      <div class="top">
        <div class="col">col</div>
        <div class="col">col</div>
        <div class="col">col</div>
      </div>
    </div>
    <div class="bottom">bottom</div>
  </footer>
</template>

<script>
export default {
  name: "AvadaFooter",
};
</script>

<style lang="scss" scoped>
footer {
  height: 400px;
  color: white;
  background-color: black;

  .top {
    display: flex;
    justify-content: space-between;

    .col {
      width: 30%;
      background-color: red;
    }
  }

  .bottom {
      text-align: center;
  }
}
</style>