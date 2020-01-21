

// I am using this component to test the page being able to load

<template>
  <p>hello</p>
</template>

<script>
export default {
name: 'film-list',
props: [films],
componenets: {
    "list-film": listFilm
},
methods: {

},

mounted() {
    fetch("https://api.punkapi.com/v2/beers")
      .then(beersData => beersData.json())
      .then(beers => (this.beers = beers));

}
</script>

<style>

</style>
