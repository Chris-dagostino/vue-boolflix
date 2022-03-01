<template>
  <main>
    <filmsList :films='films' ></filmsList>

  </main>
</template>

<script>
  
import FilmsList from './FilmsList.vue'

export default {
  name: 'MyMain',
  props: {
    'films': Array,
  },
  components: {
    FilmsList
  },
  data(){
    return{
      
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
  main{
    width: 100vw;
    height: calc(100vh - 100px );
    background-color: rgb(160, 160, 160);
  }

</style>
