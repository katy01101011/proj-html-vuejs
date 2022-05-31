<template>
  <div>
    <!-- class="menuList show" -->
    <AvadaMenuList :links="menuLinks" />
    <header id="top" :class="{ active: scrolled() }">
      <div class="header">
        <a href="">
          <img src="../assets/avadabarbers-logo-x2-200x70.png" alt="" />
        </a>
        <nav>
          <button @click="menuEvents()" class="cart" href="">
            <i class="fas fa-shopping-cart"></i>
          </button>
          <button
            @click="
              menuEvents();
              menuClicked();
            "
            class="menu"
            href=""
          >
            <i class="fas fa-bars"></i>
          </button>
        </nav>
      </div>
    </header>
  </div>
</template>

<script>
import AvadaMenuList from "./AvadaMenuList.vue";

export default {
  name: "AvadaHeader",
  components: {
    AvadaMenuList,
  },
  data() {
    return {
      iconClicked: false,
      scroll: "",
      menuLinks: [
        {
          name: "Home",
          url: "#",
          linkClicked: true,
        },
        {
          name: "About Us",
          url: "#",
          linkClicked: false,
        },
        {
          name: "Services",
          url: "#",
          linkClicked: false,
        },
        {
          name: "Shop",
          url: "#",
          linkClicked: false,
        },
        {
          name: "Our Team",
          url: "#",
          linkClicked: false,
        },
        {
          name: "Blog",
          url: "#",
          linkClicked: false,
        },
        {
          name: "Contact Us",
          url: "#",
          linkClicked: false,
        },
      ],
    };
  },
  methods: {
    // menuClicked() {
    //   this.iconClicked = true;
    //   if ((this.iconClicked = true)) {
    //   }
    // },

    menuEvents() {
      event.preventDefault();
    },

    // Questo sarebbe da fare con il computed
    scrolled() {
      window.onscroll = function () {
        const appHeader = document.getElementById("top");
        if (window.scrollY > 0) {
          this.scroll = true;
          appHeader.classList.add("active");
        } else {
          this.scroll = false;
          appHeader.classList.remove("active");
        }
      };
    },
  },
};
</script>

<style lang="scss" scoped>
@import "../style/variables";

.menuList {
  width: 100%;
  height: 100vh;
  position: fixed;
  z-index: 1001;
  background-color: black;
  color: white;
  display: none;

  button {
    border: none;
    background-color: transparent;
    margin: 1rem;
    padding: 1rem;
    cursor: pointer;
    color: white;
    position: absolute;
    top: 0;
    right: 0;
  }

  ul {
    width: 100%;
    height: 100%;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;

    li {
      padding: 1rem;
    }
  }
}

// .show {
//   display: block;
// }

.active {
  height: $header-active-height;
  background-color: $header-bg;
  transition: 0.7s;
}

header {
  width: 100%;
  height: $header-height;
  position: fixed;
  z-index: 1000;
  top: 0;
  left: 0;
  transition: 0.7s;

  .header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    width: 79%;
    margin: 0 auto;
    height: 100%;

    nav {
      width: auto;
      height: auto;
      display: flex;
      align-items: center;

      button {
        border: none;
        background-color: transparent;
        margin: 0 0.6rem;
        cursor: pointer;
        font-size: 1.5rem;
        padding: 0.5rem 0 0.5rem 0.5rem;
        display: flex;
      }

      .cart {
        color: $white;

        i {
          font-size: 1rem;
        }
      }

      .menu {
        color: $teak-brown;
      }
    }
  }
}
</style>