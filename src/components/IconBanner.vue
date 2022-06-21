<template>
    <div class="banner p-5">
        <div class="container">
            <ul>
                <li v-for="icon in icons" :key="icon">
                    <img :src="`../assets/img/buy-${icon.iconName}.${icon.extension}`" alt="">
                </li>
            </ul>
        </div>
    </div>
</template>

<script>


    export default {
        name : "IconBanner",
        data(){
            return{
                icons : [
                    {
                    iconName : "comics-digital-comics",
                    extension : "png",
                    },
                    {
                    iconName : "comics-merchandise",
                    extension : "png",
                    },
                    {
                    iconName : "comics-shop-locator",
                    extension : "png",
                    },
                    {
                    iconName : "comics-subscriptions",
                    extension : "png",
                    },
                    {
                    iconName : "dc-power-visa",
                    extension : "svg",
                    }
                    
                    
                    
                
                
                
                ]
            }
        }
    }
</script>

<style lang="scss" scoped>
@import "../assets/style/main.scss";

.banner {
    background-color: $light-blue;
}

</style>