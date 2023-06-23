<script>
export default {
    
}
</script>
<template lang="">
    <div>
        <div class="big_loader">
            <div class="loader">
                <div class="line"></div><div class="ballin"></div>
            </div>

        </div>
    </div>
</template>
<style lang="scss" scoped>

    .big_loader{
        position: fixed;
        top: 0;
        right: 0;
        width: 100vw;
        height: 100vh;
        background-color: rgb(255, 136, 0);
        display: flex;
        justify-content: center;
        align-items: center;
        flex-direction: column;
    }

    .loader {
    border: 3px solid #000000;
    border-radius: 50%;
    background: rgb(246,246,246);
    background: linear-gradient(0deg, rgba(246,246,246,1) 51%, rgba(237,58,26,1) 52%);
    width: 120px;
    height: 120px;
    -webkit-animation: spin 2s linear infinite; /* Safari */
    animation: spin 2s linear infinite;

        .ballin{
            border: 2px solid black;
            width: 20px;
            height: 20px;
            border-radius: 50%;
            position: absolute;
            top:39%;
            left:41%;
            background-color: white;
        }

        .line{
            width: 115px;
            height: 1px;
            border: 2px solid black;
            position: absolute;
            top: 45%;
            left: 0%;
        }
    }

    /* Safari */
    @-webkit-keyframes spin {
    0% { -webkit-transform: rotate(0deg); }
    100% { -webkit-transform: rotate(360deg); }
    }

    @keyframes spin {
    0% { transform: rotate(0deg); }
    100% { transform: rotate(360deg); }
    }
</style>