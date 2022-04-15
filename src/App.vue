<template>
  <Header />
  <main>
    <Photo :photos="photos" :selected="selected" />
    <Filters />
  </main>
  <Footer />
</template>

<script>
import Header from "./components/Header.vue";
import Photo from "./components/Photo.vue";
import Filters from "./components/Filters.vue";
import Footer from "./components/Footer.vue";

export default {
  name: "App",
  components: {
    Header,
    Photo,
    Filters,
    Footer,
  },
  data() {
    return {
      selected: 5,
    };
  },
  created() {
    this.photos = [
      "./src/assets/car.jpg",
      "./src/assets/baby.jpg",
      "./src/assets/pie.jpg",
      "./src/assets/jet.jpg",
      "./src/assets/dog.jpg",
    ];
  },
};
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=Roboto+Slab:wght@100;200;300;400;500;600;700;800;900&display=swap");

body {
  font-family: "Roboto Slab", "Gill Sans", "Gill Sans MT", Calibri,
    "Trebuchet MS", sans-serif;
  background-color: #321131;
  color: whitesmoke;
}
h1,
h2 {
  font-weight: 100;
}
</style>
