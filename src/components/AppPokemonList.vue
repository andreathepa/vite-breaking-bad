<script>
import AppPokemon from './AppPokemon.vue';
import { store } from '../store.js';
import AppLoader from './AppLoader.vue';
import AppResult from './AppResult.vue'

export default {
    components:{
        AppPokemon,
        AppLoader,
        AppResult
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
                <div class="col-12 mb-5">
                </div>
            </div>
            <AppLoader v-else/>
        </div>
        <AppResult />
    </div>
</template>
<style lang="scss" scoped>
    .height{
        height: 491px;

    }

    
</style>