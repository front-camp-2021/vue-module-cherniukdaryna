<template>
  <section class="filters-default">
    <div class="header-filters">
        <b class="header-filters__name">Filtres</b> 
        <a class="header-filters__back" href="#">
            <img class="header-filters__image-back-arrow" src="@/assets/img/4829860_arrow_back_left_icon.svg" />
        </a> 
    </div>

    <div class="filters-navigation">
      <div class="second-filtres-list">
        <p class="second-filtres-list__name--bold"><b>Category</b></p>

        <filters-list />
      </div>

      <img class="filters-navigation__line" src="@/assets/img/Divider.png" /><br />

      <div class="second-filtres-list">
        <p class="second-filtres-list__name--bold"><b>Brand</b></p>

        <filters-list />
      </div>
    </div>

    <button class="filters-default__buttonn-clear-all">Clear all filters</button>
  </section>
</template>

<script>
import FiltersList from './FiltersList.vue';

export default {
  name: 'SideBar',
  components: {FiltersList}
}
</script>

<style lang="scss" scoped>
  @import url("https://fonts.googleapis.com/css2?family=Barlow:wght@200&display=swap");

  .filters-default {
    width: 28.57vw;
    height: 157.35vh;
    position: relative;
    display: flex;
    justify-content: flex-start;
    flex-direction: column;
    align-items: flex-start;
    margin-left: 1vw;
    box-sizing: border-box;

    &__buttonn-clear-all {
      width: 100%;
      height:  5.2vh;
      font-size: 2rem;
      font-weight: 500;
      position: absolute;
      bottom: 0;
      background-color: #6F64F8;
      box-shadow: 0 10px 20px rgba(0,0,0,0.25), 0 5px 5px rgba(0,0,0,0.22);  
      border-radius: 8px;
      color: white;
      box-sizing: border-box;
      border: none;
      font-family: "Barlow", sans-serif;
    }
  }
  .filters-navigation {
    width: 100%;
    height: 140.83vh;
    font-size: 1.3rem;
    font-weight: 500;
    padding: 1.5vh 2.5vw;
    box-shadow: 0 10px 20px rgba(0,0,0,0.25), 0 5px 5px rgba(0,0,0,0.22);
    border-radius: 8px;
    background-color: white;
    box-sizing: border-box;

    &__line {
      width: 100%;
      height: auto;
      margin: 3.2vh 0;
    }
  }

  .header-filters {
    display: flex;
    justify-content: space-between;
    flex-direction: row;
    align-items: center;
    width: 100%;
    height: 4vh;
    font-size: 1.2rem;
    font-weight: 700;
    margin-bottom: 3.3vh;

    &__image-back-arrow {
      width: 3.7vh;
      height: 3.7vh;
      box-shadow: 0 10px 20px rgba(0,0,0,0.25), 0 5px 5px rgba(0,0,0,0.22);
      border-radius: 8px;
      background-color: white;
    }
  }

  .second-filtres-list {
    width: 100%;
    height: auto;
    box-sizing: border-box;
  }

  @media screen and (max-width: 1200px ){
    .filters-default {
      position: -webkit-sticky;
      position: sticky;
      top: -7.3vh;
    }

    .filters-navigation {
      padding: 0.5vh;
      font-size: 1rem;
      font-weight: 500;
    }
  }

  @media screen and (max-width: 720px) {
    .filters-default{
      display: none;
    }
  }
</style>