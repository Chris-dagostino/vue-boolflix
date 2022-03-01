<template>
  <div id="app" >
    <MyHeader></MyHeader>
    <MyMain :films="films" ></MyMain>
  </div>
</template>

<script>
import MyHeader from './components/MyHeader.vue'
import MyMain from './components/MyMain.vue'

const axios = require('axios');

export default {
  name: 'App',
  components: {
    MyHeader,
    MyMain,
  },
  data(){
    return{
      films:[]

    }
  },
  methods:{
    doSearch(keyWord){
      console.log(keyWord);
    },
    getFilms(keyWord){
      // Make a request for a user with a given ID
      axios.get('https://api.themoviedb.org/3/search/movie?api_key=' + this.api_key + '&query=' + keyWord + '&language=' + this.language)
      .then((response)=> {
        this.films = response.data.results;
        // handle success
        console.log(response);
      })
      .catch(function (error) {
        // handle error
        console.log(error);
      }); 
    }
  }
}
</script>

<style lang="scss">

</style>
