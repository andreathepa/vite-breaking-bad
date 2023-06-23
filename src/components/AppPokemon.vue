<script>
export default {
    props:{
        myPokemon: Object
    }
}
</script>
<template lang="">
    <div class="text-center p-2 pokemon_list">
        <div class="row flex-column">
            <div class="col">
                <div class="content_img"><img :src="myPokemon.imageUrl" class="img-fluid mb-2 circular" alt="myPokemon.info"></div>
                
            </div>
            <div class="col">
                <div>{{ myPokemon.number }}</div>
                <div>{{ myPokemon.name }}</div>
                <div>{{ myPokemon.type1 }}</div>

            </div>
        </div>
    </div>
</template>
<style lang="scss" scoped>
    
   .circular {
    margin: auto;
    width: 110px;
    height: 110px;
    border-radius: 50%;
    overflow:hidden;
}
.circular img {
    width:100%;
}
</style>