<template>
    <div>
        <div class="fumetto  text-left" :style="`background-image: ${imgUrl}`">
            <img class="card-img-top" :src="imgUrl" :alt="`Fumetto della serie di ${series}`"/>
            <div class="nome-serie">{{series}}</div>
            <div class="price-type">
                <ul class="list-unstyled">
                    <li>{{price}}</li>
                    <li>{{type}}</li>
                </ul>
            </div>
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
    position: relative;

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

.price-type {
    position: absolute;
    top: 0;
    left: 0;
    bottom: 60%;
    text-align: center;
    padding: 0.8rem 0.7rem;
    background: rgba(0,0,0,0.75);
    transform: translate(-50% , -50%);
    list-style-type: none;
    color: #fff;
    display: none;
    font-size: 1.5rem;
    font-weight: bold;

}

}

.fumetto:hover .price-type  {
    display: block;
}

.text-left {
    text-align: left;
}


</style>