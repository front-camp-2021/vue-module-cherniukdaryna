<template>
  <div class="sidebar-for-720">
    <input
      class="sidebar-for-720__checkbox--disabled"
      id="menu__burger"
      type="checkbox"
    />
    <label class="sidebar-for-720__label" for="menu__burger">
      <img
        class="sidebar-for-720__burger-image"
        src="@/assets/img/2561466_menu_icon.svg"
      />
    </label>

    <div class="filters-navigation-max-720">
      <div class="filters-navigation">
        <div class="second-filtres-list">
          <p class="second-filtres-list__name--bold"><b>Category</b></p>

          <filters-list />
        </div>

        <img
          class="filters-navigation__line"
          src="@/assets/img/Divider.png"
        /><br />

        <div class="second-filtres-list">
          <p class="second-filtres-list__name--bold"><b>Brand</b></p>

          <filters-list />
        </div>
      </div>

      <button class="filters-default__buttonn-clear-all">
        Clear all filters
      </button>
    </div>
  </div>
</template>

<script>
import FiltersList from "./FiltersList.vue";

export default {
  name: "MiniSideBar",
  components: { FiltersList },
};
</script>

<style lang="scss">
@media screen and (min-width: 720px) {
  .sidebar-for-720 {
    display: none;
  }
}

@media screen and (max-width: 720px) {
  .sidebar-for-720__checkbox--disabled {
    display: none;
  }

  .filters-navigation__line{
    width: 90%;
  }

  .sidebar-for-720 {
    height: 90vh;
    width: 45vw;
    position: fixed;
    z-index: 1;
    margin: -1vh -2.2vw -1vh -1vw;
  }

  .filters-navigation-max-720 {
    visibility: hidden;
    height: 100%;
    position: relative;
    background-color: white;
    box-shadow: 0 10px 20px rgba(0, 0, 0, 0.25), 0 5px 5px rgba(0, 0, 0, 0.22);
    border-radius: 8px;
    padding-left: 2vw;
  }

  .sidebar-for-720 {
    margin-top: -10vh;

    &__label {
      margin-left: 2vw;
    }

    &__burger-image {
      height: 4vh;
      width: 4vh;
    }
    &__close {
      height: 4vh;
      width: 4vh;
      margin-left: -4vh;
    }
  }

  .sidebar-for-720__checkbox--disabled:checked ~ .filters-navigation-max-720 {
    visibility: visible;
  }

  .filters-default__buttonn-clear-all {
    width: 100%;
    height: 5.2vh;
    font-size: 2rem;
    font-weight: 500;
    position: absolute;
    bottom: 0;
    background-color: #6f64f8;
    box-shadow: 0 10px 20px rgba(0, 0, 0, 0.25), 0 5px 5px rgba(0, 0, 0, 0.22);
    border-radius: 8px;
    color: white;
    box-sizing: border-box;
    border: none;
    font-family: "Barlow", sans-serif;
    margin-left: -2vw;
  }
}

@media screen and (max-width: 480px) {
  .sidebar-for-720 {
    width: 70vw;
  }
}

@media screen and (max-width: 320px) {
  .sidebar-for-720 {
    width: 1005;
  }
}
</style>