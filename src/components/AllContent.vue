<template>
  <div class="all-content">
    <side-bar />

    <content-component :activePage="page"/>

    <footer-pagination @page="onPage" />
  </div>
</template>

<script>
import ContentComponent from "./ContentComponent.vue";
import FooterPagination from "./FooterPagination.vue";
import SideBar from "./SideBar.vue";

export default {
  name: "AllContent",

  components: { SideBar, FooterPagination, ContentComponent },

  data() {
    return {
      page: 1,
    };
  },

  methods: {
    onPage(value) {
      this.page = value;
    },
  },
};
</script>

<style lang="scss">
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

@media screen and (max-width: 480px) {
  .all-content {
    width: 100%;
    height: 465vh;
  }
}
</style>
    