<template>
    <div>
        <div class="card" style="width: 18rem;">
            <img class="card-img-top" :src="imgUrl" :alt="`Fumetto della serie di ${series}`"/>
            <div class="card-body">
                <h5 class="card-title">Card title</h5>
                <p class="card-text">Some quick example text to build on the card title and make up the bulk of the card's content.</p>
                <a href="#" class="btn btn-primary">Go somewhere</a>
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

</style>