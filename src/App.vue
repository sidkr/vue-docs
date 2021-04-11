<template>
  <div id="app">
    <Header />
    <LeftNav />
    <div id="layout">
      <router-view />
    </div>
  </div>
</template>

<script>
import "./../node_modules/purecss/build/pure-nr-min.css"; //TODO: Alias this path
import "./styles/main.scss";
import LeftNav from "./components/LeftNav";
import Header from "./components/Header";

export default {
  name: "app",
  components: {
    LeftNav,
    Header,
  },
};
</script>

<style lang="scss"></style>
