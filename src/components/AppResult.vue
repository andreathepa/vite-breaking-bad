<script>
import { store } from '../store.js';


export default {
    data(){
        return{
          store
        }
    
    },
}
</script>
<template lang="">
    <div class="text-center mt-4">
        Found {{ store.pokemonList.length }} pokemon
    </div>
</template>
<style lang="scss" scoped>
    
</style>