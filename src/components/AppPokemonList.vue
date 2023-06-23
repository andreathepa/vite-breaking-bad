<script>
import AppPokemon from './AppPokemon.vue';
import { store } from '../store.js';

export default {
    components:{
        AppPokemon
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
            <div class="row justify-content-center height overflow-auto p-2 bg-secondary">
                <div v-for="(pokemon,index) in store.pokemonList" :key="pokemon.name" class="col-sm-12 col-md-6 col-lg-3">
                    <AppPokemon :myPokemon="pokemon"/>
                </div>
            </div>
        </div>
    </div>
</template>
<style lang="scss" scoped>
    .height{
        height: 491px;

    }

    
</style>