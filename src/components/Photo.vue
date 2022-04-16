<template>
  <div class="buttons">
    <button class="button" :disabled="selected < 1" v-on:click="selected -= 1">
      Prev
    </button>
    <button
      class="button"
      :disabled="selected > photos.length - 2"
      v-on:click="selected += 1"
    >
      Next
    </button>
  </div>

  <div>
    <img
      :src="[photos[selected]]"
      :alt="photo"
      style="
         {
          filter: `blur(4px) `;
        }
      "
    />
  </div>
  <Filters :filters="filters" />
</template>

<script>
import Filters from "./Filters.vue";

export default {
  name: "Photo",
  selection: 0,
  components: { Filters },

  props: {
    photos: Array,
    selected: Number,
    filters: Array,
  },
  methods: {
    prevPhoto() {
      this.selected -= 1;
      console.log(this.selected);
    },
    nextPhoto() {
      this.selected += 1;
    },
  },
};
</script>

<style scoped>
.buttons {
  /* border: 1px solid white; */
  display: flex;
  justify-content: flex-end;
  margin: 0px;
}
img {
  width: 100%;
}

button {
  padding: 2px 6px;
  margin: 5px 2px;
}

.off {
  background-color: gray;
}
</style>
