<template>
  <nav class="top-navigation">
    <img
      class="top-navigation__image-home"
      src="@/assets/img/3844435_home_house_icon.svg"
    />

    <img
      class="top-navigation__arrow"
      src="@/assets/img/4829859_arrow_next_right_icon.svg"
    />

    <a class="top-navigation__link" href="#">eCommerce</a>

    <img
      class="top-navigation__arrow"
      src="@/assets/img/4829859_arrow_next_right_icon.svg"
    />

    <a class="top-navigation__link" href="#">Electronics</a>
  </nav>
</template>

<script>
export default {
  name: "Navigation",
};
</script>

<style lang="scss" scoped>
.top-navigation {
  width: 90%;
  height: 2vh;
  display: flex;
  justify-content: flex-start;
  flex-direction: row;
  align-items: center;
  margin-bottom: 3.3vh;
  padding-left: 1vh;

  &__image-home {
    width: 2vw;
    height: 2vh;
  }

  &__arrow {
    width: 1.5vw;
    height: 1.5vh;
  }

  &__link:link {
    color: #7e72f2;
    font-size: 1rem;
    font-weight: 700;
    text-decoration: none;
  }

  &__link:hover {
    text-decoration: underline;
  }
}

@media screen and (max-width: 1200px) {
  .top-navigation__image-home {
    width: 3vw;
    height: 3vw;
  }

  .top-navigation__arrow {
    margin: 0 1vw;
    width: 2vw;
    height: 2vw;
  }
}

@media screen and (max-width: 720px) {
  .top-navigation {
    justify-content: center;
  }
}

@media screen and (max-width: 320px) {
  .top-navigation__image-home,
  .top-navigation__arrow {
    width: 2vh;
    height: 2vh;
  }
}
</style>