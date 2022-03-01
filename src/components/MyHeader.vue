<template>
  <header>
    <a href="#">
      <h1 class="title">Boolflix</h1>
    </a>
    <form class="contSearch">
      <input type="text" v-model="searchText" placeholder="cerca un film o serie tv...">
      <div class="search" >
        <a href="#" @click.prevent="$emit('search',searchText)" >cerca</a>
      </div>
    </form>
  </header>
</template>

<script>
export default {
  name: 'MyHeader',
  data(){
    return{
      searchText:''
      
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
  header{
    width: 100%;
    height: 100px;
    background-color: #000;
    display: flex;
    align-items: center;
    justify-content: space-around;
    a{
      text-decoration: none;
      .title{
        text-transform: uppercase;
        color: red;
    }
    }
    .contSearch{
      display: flex;
      input{
        width: 300px;
        padding: 5px;
        border-radius: 25px;
        &:hover{
          transition: 2s;
          font-size: 70px;
        }
      }
      .search{
        display: flex;
        justify-content: center;
        align-items: center;
        &:hover {
          background-color: rgb(255, 255, 255);
          transition: 2s;
          border-radius: 25px;
        }
        a{
          text-decoration: none;
          padding: 5px;
          color: rgb(241, 3, 3);
          font-weight: bolder;
          font-size:20px ;
          &:hover{
            color: #000;
            transition: 4s;
          }
        }
      }
    }
  }

</style>
