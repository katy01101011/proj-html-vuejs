<template>
  <footer>
    <div class="container">
      <div class="top">
        <AvadaFooterSideCol :side="side[0]" />
        <AvadaFooterCenterCol :centerData="centerData" />
        <AvadaFooterSideCol :side="side[1]" />
      </div>
    </div>
    <div class="bottom">
      <span>
        &copy; Copyright 2012 - 2022 | Avada Theme by <a href="">ThemeFusion</a> | All Rights Reserved | Powered by <a href="">WordPress</a>
      </span>
    </div>
  </footer>
</template>

<script>
import AvadaFooterSideCol from "../components/AvadaFooterSideCol.vue";
import AvadaFooterCenterCol from "../components/AvadaFooterCenterCol.vue";
export default {
  name: "AvadaFooter",
  components: {
    AvadaFooterSideCol,
    AvadaFooterCenterCol
  },
  data() {
    return {
      side: [
        {
          img: require("../assets/avadabarbers_footer_shop_image-400x312.png"),
          btn: "Shop our range now",
        },
        {
          img: require("../assets/avadabarbers_footer_appointment_image-400x312.png"),
          btn: "Book your appointment",
        },
      ],
      centerData: {
        info: [
          "Avada Barbers",
          "123 New York Street",
          "New York City",
          "info@yourwebsite.com",
          "+1(555)555-1212",
        ],
        social: [
          "fa-facebook-f",
          "fa-twitter",
          "fa-instagram",
          "fa-youtube",
        ],
      },
    }
  },
};
</script>

<style lang="scss" scoped>
@import "../style/variables";
footer {
  color: white;
  background-color: black;
  .top {
    display: flex;
    justify-content: space-between;
  }
  .bottom {
      height: $footer-bottom-height;
      line-height: $footer-bottom-height;
      text-align: center;
      background-color: $cod-gray-black;
      
      span {
        color: $text-details;
        font-size: .85rem;
        a {
          color: $text-secondary;
          text-decoration: none;
        }
      }
  }
}
</style>