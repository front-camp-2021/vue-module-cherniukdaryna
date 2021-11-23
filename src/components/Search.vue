<template>
  <div class="search">
    <input
      class="search__input"
      type="search"
      id="search"
      placeholder="  Search"
      v-model="searchValue"
      @keyup="setInput(searchValue)"
    />

    <button class="search__btn-glass">
      <img
        class="search__image-search"
        src="@/assets/img/4801315_glass_magnifier_magnifying_search_searching_icon.svg"
      />
    </button>
  </div>
</template>

<script>
export default {
  name: "Input",
  
  data(){
    return {
      search: ''
    }
  },

  methods: {
    setInput(value){
      this.$emit('search', value);
    }
  }
};
</script>

<style lang="scss" scoped>
.search {
  width: 100%;
  height: 5.75vh;
  display: flex;
  justify-content: space-between;
  flex-direction: row;
  align-items: flex-start;

  &__input {
    width: 90%;
    height: 100%;
    border-radius: 8px;
    box-shadow: 0 10px 20px rgba(0, 0, 0, 0.25), 0 5px 5px rgba(0, 0, 0, 0.22);
    font-size: 1.7rem;
    font-weight: 500;
    border: none;
  }

  &__btn-glass {
    width: 2.8vw;
    height: 100%;
    border-radius: 8px;
    box-shadow: 0 10px 20px rgba(0, 0, 0, 0.25), 0 5px 5px rgba(0, 0, 0, 0.22);
    border: none;
  }

  &__image-search {
    width: 2vw;
    height: 4vh;
  }

  @media screen and (max-width: 1200px) {
    .search__btn-glass {
      width: 4vw;
    }

    .search__image-search {
      width: 3vw;
      height: 5vh;
    }
  }

  @media screen and (max-width: 720px) {
    .search__btn-glass {
      width: 6vw;
      height: 100%;
    }
  }

  @media screen and (max-width: 480px) {
    .search {
      margin-bottom: 3vh;
    }

    .search {
      &__input {
        width: 80%;
        height: 100%;
      }
    }
    .search__btn-glass {
      width: 8vw;
      height: 100%;
    }
  }
}
</style>