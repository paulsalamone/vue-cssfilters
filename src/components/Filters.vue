<template>
  <h2>filters:</h2>
  <div :key="filter.id" v-for="filter in filters">
    <p>• {{ filter.id }}</p>
  </div>
</template>

<script>
export default {
  name: "Filter",
  props: {
    filters: Array,
  },
};
</script>

<style></style>
