<template>
  <a class="links-list__link" :id="isActive" href="#">{{ pageItem }}</a>
</template>

<script>
export default {
  name: "PageItem",

  props: {
    pageItem: {
      type: Array,
      requier: false,
    },
    isActive: {
      type: String,
      requier: false,
    },
  },
};
</script>

<style lang="scss">
.links-list__link:link {
  width: 2.04vw;
  height: 2.04vw;
  border-radius: 50%;
  display: flex;
  justify-content: center;
  flex-direction: row;
  align-items: center;
  background-color: rgba(237, 237, 237, 1);
  text-decoration: none;
  color: black;
}
.links-list__link:hover,
.links-list__link:active {
  background-color: #6f64f8;
  color: white;
  text-decoration: none;
}

#active {
  background-color: #6f64f8;
  color: white;
  text-decoration: none;
}

@media screen and (max-width: 1200px) {
  .links-list {
    &__link:link {
      width: 4vw;
      height: 4vw;
    }
  }
}

@media screen and (max-width: 480px) {
  .links-list {
    &__link:link {
      width: 2.5vh;
      height: 2.5vh;
    }
  }
}
</style>