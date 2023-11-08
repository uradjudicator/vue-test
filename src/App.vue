<template >
  <div class="app font-monospace">
    <div class="content">
      <AppInfo :allMoviesCount="movies.length" :favouriteMoviesCount="movies.filter(c => c.favourite).length"/>
      <div class="search-panel">
        <searchPanel />
        <AppFilter />
      </div>
      <MovieList :movies="movies"/>
      <movieAddForm />
    </div>
  </div>
</template>
<script>
  import AppInfo from "@/components/app-info.vue"
  import searchPanel from "./components/searchPanel.vue";
  import AppFilter from "./components/AppFilter.vue"
  import MovieList from "./components/movieList.vue"
  import movieAddForm from "./components/movieAddForm.vue";
export default {
  components:{
    AppInfo,
    searchPanel,
    AppFilter,
    MovieList,
    movieAddForm
 },
 data() {
        return {
            movies: [
                {
                    name: 'John Wick 4', 
                    viewers:'458',
                    favourite:false,
                    like: true
                },
               {
                    name: 'Fast and Furious X', 
                    viewers:'633',
                    favourite:false,
                    like: false
                },
                {
                    name: 'Hobs & Shaw 2', 
                    viewers:'571',
                    favourite:true,
                    like: false
                },
               
            ]
        }
    }
}
</script>
<style>
  .app
  {
    height: 100%;
  }
  .content{
    width: 1000px;
    min-height: 700px;
    background-color: #333;
    margin: 0 auto;
    padding: 5rem 0;
  }

  .search-panel{
    margin-top: 2rem;
    padding: 1.5rem;
    background-color: #fcfaf5;
    border-radius: 4px;
    box-shadow: 15px 15px 15px rgba(0,0,0,0.15);
  }
</style>
