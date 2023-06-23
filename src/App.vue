<script>
import AppHeader from './components/AppHeader.vue';
import AppPokemonList from './components/AppPokemonList.vue';

export default {
    components:{
      AppHeader,
      AppPokemonList
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