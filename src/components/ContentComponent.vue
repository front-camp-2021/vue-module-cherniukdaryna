<template>
  <div class="content">
    <results />

    <search @search="onSearch"/>

    <cards-list 
    :currentPage="activePage" 
    :categories="activeCategory" 
    :brands="activeBrands"
    :input="inputValue"/>
  </div>
</template>

<script>
import CardsList from "./CardsList.vue";
import Results from "./Results.vue";
import Search from "./Search.vue";
export default {
  name: "ContentComponent",

  components: { Search, Results, CardsList },

  data(){
    return {
      inputValue: ''
    }
  },

  props: {
    activePage:{
      type: Number,
      requier: false,
    },

    activeCategory:{
      type: Array,
      requier: false,
    },

    activeBrands:{
      type: Array,
      requier: false,
    },
  },

  methods: {
    onSearch(value){
      this.inputValue = value;
    }
  }
};
</script>

<style lang="scss">
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
  .content {
    margin: 0 2vw;
  }
}
</style>