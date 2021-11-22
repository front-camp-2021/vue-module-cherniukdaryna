<template>
  <div id="app">
    <header-logo />

    <navigation />

    <side-bar-mini />

    <all-content />
  </div>
</template>

<script>
import AllContent from './components/AllContent.vue';
import HeaderLogo from "./components/HeaderLogo.vue";
import Navigation from "./components/Navigation.vue";
import SideBarMini from './components/SideBarMini.vue';

export default {
  name: "App",
  components: {
    Navigation,
    HeaderLogo,
    SideBarMini,
    AllContent
  },
};
</script>

<style lang="scss" scoped>
@import url("https://fonts.googleapis.com/css2?family=Barlow:wght@200&display=swap");
#app {
  box-sizing: border-box;
  margin: -5px;
  padding: 0;
  border: 8px;
  font-family: "Barlow", sans-serif;
  text-decoration: none;
  font-size: 95%;
  background-color: rgba(249, 249, 249, 0.911);
  color: black;
}


</style>



