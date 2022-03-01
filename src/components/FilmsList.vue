<template>
    <section>
        <ul>
            <FilmCard v-for="(film,index) in films" :key="index" :film='film' >

            </FilmCard>
        </ul>
    </section>
</template>

<script>

import FilmCard from './partials/FilmCard.vue';

export default {
    name: "FilmsList",
    props: {
        'films': Array
  },
  components: {
      FilmCard
  }
}

</script>

<style>

</style>