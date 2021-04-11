<template>
  <div>
    <!-- Menu toggle -->
    <a
      href="#"
      id="menuLink"
      class="menu-link"
      @click="toggleMenu()"
      :class="{ active: showMenu }"
    >
      <span> ☰ </span>
    </a>

    <div class="menu" :class="{ active: showMenu }">
      <div class="pure-menu">
        <a class="pure-menu-heading" href="#">Vue Docs</a>

        <ul class="pure-menu-list">
          <li class="pure-menu-item">
            <router-link to="/" class="pure-menu-link">Home</router-link>
          </li>
          <li class="pure-menu-item">
            <router-link to="/about" class="pure-menu-link">About</router-link>
          </li>

          <li class="pure-menu-item menu-item">
            <a href="#" class="pure-menu-link">Services</a>
          </li>

          <li class="pure-menu-item">
            <a href="#contact" class="pure-menu-link">Contact</a>
          </li>
        </ul>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "left-nav",
  data() {
    return {
      showMenu: false,
    };
  },
  methods: {
    toggleMenu() {
      this.showMenu = !this.showMenu;
    },
  },
};
</script>

<style lang="scss">
.menu {
  &.active {
    left: 250px;
  }
}

.menu-link {
  &.active {
    left: 250px;
  }
}

.pure-menu-item {
  a.router-link-active {
    background: #1f8dd6;
    color: white;
  }
}
</style>
