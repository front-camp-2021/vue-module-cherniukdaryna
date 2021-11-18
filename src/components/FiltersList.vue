<template>
  <form
    class="second-filtres-list__form"
    action=""
    method="GET"
    name="category"
  >
    <filter-item />
  </form>
</template>

<script>
import FilterItem from "./FilterItem.vue";

export default {
  name: "FiltersList",
  components: { FilterItem },
};
</script>

<style lang="scss" scoped>
.second-filtres-list {
  &__form {
    display: flex;
    justify-content: space-between;
    flex-direction: row;
    align-items: start;
    margin-top: 1.8vh;
  }
}
</style>
