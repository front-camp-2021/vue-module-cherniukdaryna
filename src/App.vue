<template>
  <div id="app">
    <header-logo />

    <navigation />

    <side-bar-mini />

    <div class="all-content">
      <side-bar />
      <div class="content">
        <results />

        <search />

        <cards-list />
      </div>

      <footer-pagination />
    </div>
  </div>
</template>

<script>
import CardsList from "./components/CardsList.vue";
import FooterPagination from './components/FooterPagination.vue';
import HeaderLogo from "./components/HeaderLogo.vue";
import Navigation from "./components/Navigation.vue";
import Results from "./components/Results.vue";
import Search from "./components/Search.vue";
import SideBar from './components/SideBar.vue';
import SideBarMini from './components/SideBarMini.vue';

export default {
  name: "App",
  components: {
    Navigation,
    HeaderLogo,
    Results,
    CardsList,
    Search,
    SideBar,
    FooterPagination,
    SideBarMini,
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

.all-content {
  width: 100%;
  height: auto;
  display: -webkit-box;
  display: -ms-flexbox;
  display: flex;
  -webkit-box-pack: justify;
  -ms-flex-pack: justify;
  justify-content: space-between;
  -webkit-box-orient: horizontal;
  -webkit-box-direction: normal;
  -ms-flex-direction: row;
  flex-direction: row;
  -webkit-box-align: start;
  -ms-flex-align: start;
  align-items: flex-start;
  position: relative;
  padding-bottom: 8vh;
}

.content {
  height: 157.35vh;
  display: flex;
  justify-content: space-between;
  flex-direction: column;
  align-items: center;
  margin-bottom: 5vh;
  margin-right: 2vw;
}

@media screen and (max-width: 1200px) {
  .content {
    width: 63vw;
    height: 253.35vh;
  }
}

@media screen and (max-width: 720px) {
  .content {
    width: 100%;
    height: 253.35vh;
    padding-left: 2vw;
  }
}

@media screen and (max-width: 480px) {
  .all-content {
    width: 100%;
    height: 465vh;
  }

  .content {
    margin: 0 2vw;
  }
}
</style>



