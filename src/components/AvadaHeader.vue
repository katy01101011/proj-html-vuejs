<template>
  <div>
    <!-- class="menuList show" -->
    <div id="ok" class="menuList" :class="{ show: iconClicked }">
      <div>
        <button @click="menuClicked">
          <i class="fas fa-times"></i>
        </button>
      </div>
      <ul>
        <li
          v-for="(link, index) in menuLinks"
          :key="index"
          :class="{ activeListItem: link.linkClicked === true }"
        >
          {{ link.name }}
        </li>
      </ul>
    </div>
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
export default {
  name: "AvadaHeader",
  components: {},
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
    menuClicked() {
      this.iconClicked = !this.iconClicked;
    },
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
  z-index: 10001;
  background-color: $header-bg;
  color: white;
  font-size: 1.5rem;
  display: none;
  button {
    border: none;
    background-color: transparent;
    margin: 0.6rem 0.8rem;
    padding: 1rem;
    cursor: pointer;
    color: white;
    position: absolute;
    top: 0;
    right: 0;
    font-size: inherit;
    transition: 0.7s;
  }
  button:hover {
    color: $text-hover;
    transition: 0.7s;
  }
  ul {
    width: 100%;
    height: 100%;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    li {
      width: 100%;
      text-align: center;
      margin: 0.25rem;
      padding: 1rem;
      cursor: pointer;
      transition: 0.7s;
    }
    li:hover {
      color: $text-hover;
      transition: 0.7s;
    }
    // li:hover .menuList {
    //   background-color: red;
    // }
    .activeListItem {
      color: $text-hover;
    }
  }
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
.show {
  display: block;
}
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
    width: 70%;
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
          transition: 0.6s;
        }
        i:hover {
          color: $text-hover;
          transition: 0.6s;
        }
      }
      .menu {
        color: $teak-brown;
      }
    }
  }
}
</style>