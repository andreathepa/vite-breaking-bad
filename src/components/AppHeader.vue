<script>
export default {
    props:{
        title: String
    }
}
</script>
<template lang="">
    <header class="container">
        <h1 class="text-center my-5"> {{ title }} </h1>
    </header>
</template>
<style lang="scss" scoped>
    h1{
        font-weight: 700;
    }

    
</style>