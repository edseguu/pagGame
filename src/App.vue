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

            <button class="buttonDownload">DESCARGAR: Alpha1</button>
            
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
        
        width: 100%;
        text-align: center;
        font-size: clamp(4rem, 2.5vw, 2rem);
        text-shadow: 4px 5px 5px var(--silver-lake-blue);

        margin-bottom: 10%;

    }
    .container_body{
        justify-content: center;
        display: flex;
        gap: 1%;
    }

    h1{
        color: var(--platinum);
        text-align: center;
        font-size: clamp(1rem, 22.5vw, 2rem);
    }
    button{
        display: block;
        margin: 10% auto;

        font-size: clamp(1rem, 22.5vw, 2rem);
    }




    /* From Uiverse.io by dovatgabriel */ 
    .buttonDownload {
    display: block;
    position: relative;
    padding: 10px 25px;
    background-color: #41961a;
    color: var(--platinum);
    font-family: sans-serif;
    text-decoration: none;
    font-size: clamp(1rem, 22.5vw, 2rem);
    text-align: center;
    text-indent: 15px;
    border: none;
    cursor: pointer;
    }

    .buttonDownload:hover {
    background-color: #316e15;
    color: white;
    }

    .buttonDownload:before, .buttonDownload:after {
    content: ' ';
    display: block;
    position: absolute;
    left: 15px;
    top: 52%;
    }

    .buttonDownload:before {
    width: 10px;
    height: 2px;
    border-style: solid;
    border-width: 0 2px 2px;
    }

    .buttonDownload:after {
    width: 0;
    height: 0;
    margin-left: 3px;
    margin-top: -7px;
    border-style: solid;
    border-width: 4px 4px 0 4px;
    border-color: transparent;
    border-top-color: inherit;
    animation: downloadArrow 1s linear infinite;
    animation-play-state: paused;
    }

    .buttonDownload:hover:before {
    border-color: #cdefbd;
    }

    .buttonDownload:hover:after {
    border-top-color: #cdefbd;
    animation-play-state: running;
    }

    @keyframes downloadArrow {
    0% {
    margin-top: -7px;
    opacity: 1;
    }

    0.001% {
    margin-top: -15px;
    opacity: 0.4;
    }

    50% {
    opacity: 1;
    }

    100% {
    margin-top: 0;
    opacity: 0.4;
    }
    }
</style>
