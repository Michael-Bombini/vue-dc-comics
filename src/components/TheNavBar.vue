<template>
    <nav class="p-3">
        <div class="container">
            <header class="d-flex align-items-center justify-content-between">
                <img src="../assets/img/dc-logo.png" alt="">
            <ul class="nav justify-content-center">
                <li class="nav-item" v-for="link in linkNav" :key="link">
                    <a class="nav-link active p-3" aria-current="page" href="#">{{link}}</a>
                </li>
            </ul>
            
            </header>
        </div>
    </nav>
</template>

<script>
    export default {
      name : "TheNavBar",
      data() {
        return{
            linkNav : [
                "Characters" , "Comics" , "Movies" ,
                "TV" , "Games" , "Collectibles" ,
                "Videos" , "Fans" , "News" , "Shop"
            ]
        }
      }
    }
</script>

<style lang="scss" scoped>
@import "../assets/style/main.scss";

nav {
    background-color: $white;

    ul li {
        text-transform: uppercase;
        font-size: 0.9rem;
        font-weight: bold;

      a {
        color: $light-black;
      }
      

    }



}


</style>