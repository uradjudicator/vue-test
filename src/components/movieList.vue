<template>
    <ul  class="movie-list list-group">
        
      <MovieListItem v-for="movie in movies" v-bind:movie="movie"/>
      
      
    </ul>
</template>
<script>
import MovieListItem from './movie-list-item/movie-list-item.vue';

export default {
    components: { MovieListItem},
    props:{
        movies:{
        type:Array,
        required:true
    }}
}
</script>
<style scoped>
    .movie-list{
        margin-top: 2rem;
    margin-bottom: 1rem;
    padding: 1.5rem;
    background-color: beige;
    border-radius: 4px;
    box-shadow: 15px 15px 15px rgba(0, 0, 0, 0.15);
    }
</style>