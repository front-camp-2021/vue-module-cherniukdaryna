<template>
  <footer class="footer" v-on:click="$emit(currentPage)">
    <a
      class="footer__arrow-back-left"
      href="#"
      v-on:click="
        currentPage = currentPage === 1 ? currentPage : currentPage - 1
      "
      @click="setCurrentPage"
    >
      <img
        class="footer__image-arrow-back-left"
        src="@/assets/img/2931162_arrow_back_left_direction_move_icon.svg"
      />
    </a>

    <div class="links-list">
      <page-item
        v-for="item in pageArray"
        :key="item"
        :pageItem="item"
        :isActive="item === currentPage ? 'active' : 'inactive'"
        v-on:click="currentPage = item"
        @click="setCurrentPage"
      />
    </div>

    <a
      class="footer__arrow-forward-right"
      href="#"
      v-on:click="
        currentPage = currentPage === 20 ? currentPage : currentPage + 1
      "
      @click="setCurrentPage"
    >
      <img
        class="footer__image-arrow-forward-right"
        src="@/assets/img/2931159_arrow_forward_right_move_navigation_icon.svg"
      />
    </a>
  </footer>
</template>

<script>
import PageItem from "./PageItem.vue";
export default {
  name: "Pagination",

  components: { PageItem },

  data() {
    return {
      totalPage: 20,
      currentPage: 1,
      pageArray: [],
    };
  },

  beforeMount() {
    this.getPageArray();
  },
  methods: {
    getPageArray() {
      this.pageArray = Array.from({ length: this.totalPage }, (_, i) => i + 1);
    },

    setCurrentPage() {
      this.$emit('page', this.currentPage);
    }
  },
};
</script>

<style lang="scss">
.footer {
  width: 100%;
  height: 6vh;
  font-size: 1.2rem;
  font-weight: 500;
  display: flex;
  justify-content: center;
  flex-direction: row;
  align-items: flex-start;
  position: absolute;
  bottom: 0;

  &__arrow-back-left:link,
  &__arrow-forward-right:link {
    width: 2.04vw;
    height: 2.04vw;
    border-radius: 50%;
    display: flex;
    justify-content: center;
    flex-direction: row;
    align-items: center;
    background-color: white;
    background-color: rgba(237, 237, 237, 1);
    color: black;
  }

  &__arrow-back-left:hover,
  &__arrow-forward-right:hover,
  &__arrow-back-left:active,
  &__arrow-forward-right:active {
    background-color: #6f64f8;
  }

  &__image-arrow-back-left,
  &__image-arrow-forward-right {
    width: 1vw;
    height: 2vh;
  }
}

.links-list {
  display: flex;
  justify-content: center;
  flex-direction: row;
  align-items: flex-start;
  margin: 0 2vw;
  border-radius: 20px;
  width: 40.8vw;
  height: 2.04vw;
  background-color: rgba(237, 237, 237, 1);
}

@media screen and (max-width: 1200px) {
  .links-list {
    width: 80vw;
    height: 4vw;
  }

  .footer__arrow-back-left:link,
  .footer__arrow-forward-right:link {
    width: 4vw;
    height: 4vw;
  }
}

@media screen and (max-width: 480px) {
  .links-list {
    width: 50vh;
    height: 2.5vw;
  }

  .footer {
    &__arrow-back-left:link,
    &__arrow-forward-right:link {
      width: 2.5vh;
      height: 2.5vh;
    }

    &__image-arrow-forward-right,
    &__image-arrow-back-left {
      width: 1.5vh;
      height: 1.5vh;
    }
  }
}
</style>