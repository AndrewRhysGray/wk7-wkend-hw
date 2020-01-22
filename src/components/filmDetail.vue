<template>
  <div>
        <ul>
            <list-item v-for="(film, index) in films" :film="film" :key="index">
            </list-item>
        </ul>>

  </div>

</template>

<script>
    import filmItem from './filmItem.vue'
    export default {
    name: 'film-list',
    props: ['films'],
    components: {
        "filmItem": filmItem
    },
    methods: {

    }
    }
    </script>

    <style>
    </style>
