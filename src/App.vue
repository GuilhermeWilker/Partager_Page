<template>
  <div class="app">
    <Slider />
    <View />
  </div>
</template>

<script>
import Slider from "./components/Slider.vue";
import View from "./components/View.vue";

export default {
  name: "App",
  components: {
    Slider,
    View,
  },
};
</script>

<style scoped>
@import url("https://fonts.googleapis.com/css2?family=IBM+Plex+Serif:wght@100;200;300;400;500;600;700&display=swap");

.app {
  margin: 0 auto;
  padding: 15px;

  display: flex;
  justify-content: center;
  gap: 250px;

  font-family: "Roboto", sans-serif;
}

@media (max-width: 1280px) {
  .app {
    gap: 80px;
  }
}

@media (max-width: 430px) {
  .app {
    gap: 80px;
    flex-direction: column-reverse;
    justify-content: center;
    align-items: center;
  }
}
</style>
