<script>
export default {
    props:{
        title: String
    }
}
</script>
<template lang="">
    <header class="container">
        <div class="row align-items-center">
            <div class="col">
                <div class="content">
                    <div class="row">
                        <div class="ball_big"></div>

                        <div class="ball red mx-3"></div>

                        <div class="ball green"></div>

                        <div class="ball yellow mx-3"></div>
                    </div>

                </div>
            </div>
            <div class="col-7">
                <h1 class="my-5"> {{ title }} </h1>

            </div>

        </div>
    </header>
</template>
<style lang="scss" scoped>
    h1{
        font-weight: 700;
    }

    .ball_big{
        width: 50px;
        height: 50px;
        border-radius:50%;
        background: rgb(2,0,36);
        background: linear-gradient(163deg, rgba(2,0,36,1) 0%, rgba(255,255,255,1) 0%, rgba(9,133,205,1) 37%);
        border: 4px solid white;     
    }

    .ball{
        width: 30px;
        height: 30px;
        border-radius:50%;
        border: 2px solid white;     

        
    }

    .red{
        background: rgb(2,0,36);
        background: linear-gradient(163deg, rgba(2,0,36,1) 0%, rgba(255,255,255,1) 0%, rgba(205,27,9,1) 37%); 
        }

        .yellow{
            background: rgb(2,0,36);
            background: linear-gradient(163deg, rgba(2,0,36,1) 0%, rgba(255,255,255,1) 0%, rgba(205,205,9,1) 37%); 
        }

        .green{
            background: rgb(2,0,36);
            background: linear-gradient(163deg, rgba(2,0,36,1) 0%, rgba(255,255,255,1) 0%, rgba(34,205,9,1) 37%); 
        }
    
</style>