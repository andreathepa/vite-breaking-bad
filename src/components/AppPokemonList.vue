<script>
import axios from 'axios';
import AppPokemon from './AppPokemon.vue';

export default {
    components:{
        AppPokemon
    },
    data(){
        return{
            pokemonList: []
        }
    
    },
    mounted(){
        axios.get('https://41tyokboji.execute-api.eu-central-1.amazonaws.com/dev/api/v1/pokemons?per=12').then((response) => {
            this.pokemonList = response.data.docs;
        })
    } 
}
</script>
<template lang="">
    <div>
        <div class="container">
            <div class="row">
                <div v-for="(pokemon,index) in pokemonList" :key="pokemon.name" class="col-sm-6 col-md-4 border">
                    <AppPokemon :myPokemon="pokemon"/>
                </div>
            </div>
        </div>
    </div>
</template>
<style lang="">
    
</style>