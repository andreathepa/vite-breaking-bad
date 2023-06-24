<script>
import AppPokemon from './AppPokemon.vue';
import { store } from '../store.js';
import AppLoader from './AppLoader.vue';

export default {
    components:{
        AppPokemon,
        AppLoader
    },
    data(){
        return{
          store
        }
    
    } 
}
</script>
<template lang="">
    <div>
        <div class="container bg-white p-5 rounded-5">
            <div class="row justify-content-center height overflow-auto p-2 bg-secondary" v-if="store.loading === false">
                <div v-for="(pokemon,index) in store.pokemonList" :key="pokemon.name" class="col-sm-12 col-md-6 col-lg-3">
                    <AppPokemon :myPokemon="pokemon"/>
                </div>
            </div>
            <AppLoader v-else/>
        </div>
    </div>
</template>
<style lang="scss" scoped>
    .height{
        height: 491px;

    }

    
</style>