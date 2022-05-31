<template>
  <div class="menuList show">
    <div>
      <button @click="menuClicked">
        <i class="fas fa-times"></i>
      </button>
    </div>
    <ul>
      <li
        v-for="(link, index) in links"
        :key="index"
        :class="{ activeListItem: link.linkClicked === true }"
      >
        {{ link.name }}
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "AvadaMenuList",
  props: {
    links: Array,
  },
  data() {
      return {
          itemClicked: false,
      }
  },
  methods: {
    menuClicked() {
        this.itemClicked = !this.itemClicked;
        console.log(this.itemClicked);
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
  z-index: 2000;
  background-color: $header-bg;
  color: white;
  font-size: 1.5rem;

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

    .activeListItem {
      color: $text-hover;
    }
  }
}
</style>