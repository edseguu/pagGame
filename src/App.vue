<script setup>
    import { ref } from "vue";
    const images = ref([
        "/topos.png",
        "/catch.png",
        "/pinpong.png"
    ]);
    const current = ref(0);

    setInterval(() => {
        current.value = (current.value + 1) % images.value.length;
    }, 5000);

</script>

<template>
    <h1 class="title">GG RANDOM</h1>
    <div class="container_body">
        <div class="carrousel_img">
            <img :src="images[current]" alt="IMG DE REFERENCIA">
        </div>
        
        <div>
            <h1>
                Mini juegos que cambian al azar cuando pierdes.
            </h1>

            <button>DESCARGAR: Alpha1</button>
            
        </div>
        

    </div>
    
</template>

<style>
    img{
        width: 50%;
        position: relative;
        transform: translateX(50%);
    }

    .title{
        color: rgb(255, 255, 255);
        width: 100%;
        text-align: center;
        font-size: clamp(4rem, 2.5vw, 2rem);
        text-shadow: 4px 5px 5px grey;

        margin-bottom: 10%;

    }
    .container_body{
        justify-content: center;
        display: flex;
        gap: 1%;
    }

    h1, h2{
        color: rgb(255, 255, 255);
        text-align: center;
        font-size: clamp(1rem, 22.5vw, 2rem);
    }
    button{
        display: block;
        margin: 10% auto;

        font-size: clamp(1rem, 22.5vw, 2rem);
    }
</style>
