<template>
  <Button>Prev</Button>
  <Button>Next</Button>
  <br />
  <!-- <div :key="index" v-for="(photo, index) in photos">
    <img :src="photo" :key="index" />
  </div> -->
  <div>
    <h1>{{ selected }}</h1>
    <img :src="photos[selected]" />
  </div>
</template>

<script>
export default {
  name: "Photo",
  props: {
    photos: Array,
    selected: Number,
  },
};
</script>

<style scoped>
img {
  width: 100%;
}
</style>
