<template>
  <div>
    <input
      class="first-filtres-list__checkbox-input"
      type="checkbox"
      :id="filtersList"
      :name="filtersList"
    />
    <label class="first-filtres-list__checkbox-input-label" :for="filtersList">
      {{filtersList}}
    </label>
    <br />
  </div>
</template>

<script>
export default {
  name: "FilterItem",

  props: {
    filtersList: {
      type: String,
      requier: false,
    }
  }
}
</script>

<style lang="scss" scoped>

</style>
