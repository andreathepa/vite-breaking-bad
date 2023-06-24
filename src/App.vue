<script>
import AppHeader from './components/AppHeader.vue';
import AppPokemonList from './components/AppPokemonList.vue';
import { store } from './store.js';
import axios from 'axios';
import AppLoader from './components/AppLoader.vue';


export default {
    components:{
      AppHeader,
      AppPokemonList,
      AppLoader
    },
    data(){
        return{
          store,
        }
    
    },
    mounted(){
        axios.get(store.apiUrl).then((response) => {
            store.pokemonList = response.data.docs;
            store.loading = false;
        })
    }
}
</script>
<template lang="">
  <div>
    <AppHeader  class="text-light" title="Pokedex"/>
    <AppPokemonList />
  </div>
</template>
<style lang="scss">
  @use './styles/generals.scss' as *;
</style>