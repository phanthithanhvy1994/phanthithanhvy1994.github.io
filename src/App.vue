<template>
  <Header />
  <PhotoCards />
</template>

<script>
import Header from "./components/Header.vue";
import PhotoCards from "./components/PhotoCards.vue";


export default {
  name: "App",
  components: {
    Header,
    PhotoCards,
  },
};
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  // text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
