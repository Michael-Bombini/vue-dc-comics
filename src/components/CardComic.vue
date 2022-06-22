<template>
    <div>
        <div class="fumetto m-4">
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
    width: 200px;
    height: 200px;
    aspect-ratio: 1/1;

img {
    max-width: 100%;
    max-height: 100%;

}

.nome-serie {
    color: #fff;
    padding-top: 0.5rem;
    text-transform: uppercase;
}


}


</style>