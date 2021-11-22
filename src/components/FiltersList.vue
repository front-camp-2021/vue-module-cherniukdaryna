<template>
  <div>
    <div class="second-filtres-list">
      <p class="second-filtres-list__name--bold"><b>Category</b></p>

      <form
        class="second-filtres-list__form"
        action=""
        method="GET"
        name="category"
      >
        <filter-item
          v-for="item in categoriesList"
          :key="item.id"
          :filtersList="item"
        />
      </form>
    </div>

    <img
      class="filters-navigation__line"
      src="@/assets/img/Divider.png"
    /><br />

    <div class="second-filtres-list">
      <p class="second-filtres-list__name--bold"><b>Brands</b></p>

      <form
        class="second-filtres-list__form"
        action=""
        method="GET"
        name="category"
      >
        <filter-item
          v-for="item in brandsList"
          :key="item.id"
          :filtersList="item"
        />
      </form>
    </div>
  </div>
</template>

<script>
import FilterItem from "./FilterItem.vue";

export default {
  name: "FiltersList",

  components: { FilterItem },

  data() {
    return {
      categoriesList: [],
      brandsList: [],
    };
  },

  beforeMount() {
    this.getCategories();
    this.getBrands();
  },
  methods: {
    async getCategories() {
      const res = await fetch("http://localhost:3001/categories");
      const data = await res.json();
      this.categoriesList = data;
    },

    async getBrands() {
      const res = await fetch("http://localhost:3001/brands");
      const data = await res.json();
      this.brandsList = data;
    },
  },
};
</script>

<style lang="scss" scoped>
  .second-filtres-list {
    &__form {
      margin-top: 1.8vh;
      width: 100%;
      height: auto;
      box-sizing: border-box;
    }
  }
  .filters-navigation__line {
    width: 100%;
    height: auto;
    margin: 3.2vh 0;
  }
</style>
