<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png" />
    <filmList msg="Welcome to Your Vue.js App" />
  </div>
</template>

<script>
import filmList  from "./components/filmList.vue";

export default {
  name: "app",
  data() {
    return {
      Films: [],
      selectedFilms
    };
  },
  components: {
    
  },

  mounted() {
    fetch("https://ghibliapi.herokuapp.com/")
      .then(response => response.json())
      .then(data => (this.data = data));
  }
};
</script>



<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
