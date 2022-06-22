<template>
    <div>
        <div class="fumetto  text-left" :style="`background-image: ${imgUrl}`">
            <img class="card-img-top" :src="imgUrl" :alt="`Fumetto della serie di ${series}`"/>
            <div class="nome-serie">{{series}}</div>
        </div>


        
        </div>

</template>

<script>
    export default {
     name : "CardComic",
     props: {
        imgUrl : String,
        price : String,
        series : String,
        type : String,
     }
    }
</script>

<style lang="scss" scoped>


.fumetto {

    aspect-ratio: 1;

img {
    max-width: 100%;
    max-height: 100%;
        object-fit: cover;
    object-position: top right;

}

.nome-serie {
    color: #fff;
    padding-top: 0.5rem;
    text-transform: uppercase;
}


}

.text-left {
    text-align: left;
}


</style>