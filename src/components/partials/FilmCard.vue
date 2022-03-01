<template>
    <li>
        <div>{{film.title}}</div>
        <div>{{film.original_title}}</div>

        
        <div>
            <img v-if="languages.includes(film.original_language)" :src="require('../../assets/flags/' + film.original_language + '.png')" alt="">
            <!--<span v-else>{{film.original_language}}</span>-->
        </div>


        <div>{{film.vote_average}}</div>
    </li>
</template>

<script>
export default {
    name: 'FilmCard',
    props: {
        'film': Object
    },
    data(){
        return{
            language:['en', 'it']
        }
    }
}
</script>

<style>

</style>