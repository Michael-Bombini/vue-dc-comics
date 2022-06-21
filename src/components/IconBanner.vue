<template>
    <div class="banner p-5">
        <div class="container">
            <ul class="d-flex justify-content-around">
                <li v-for="icon in icons" :key="icon.iconName">
                        <img :src="require(`@/assets/img/buy-${icon.iconName}.${icon.extension}`)" alt="icon.iconName">
                        <span>{{icon.title}}</span>

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
                    title : "DIGITAL COMICS",
                    },
                    {
                    iconName : "comics-merchandise",
                    extension : "png",
                    title : "DC MERCHANDDISE",
                    },
                    {
                    iconName : "comics-shop-locator",
                    extension : "png",
                    title : "SUBSCRIPTION",
                    },
                    {
                    iconName : "comics-subscriptions",
                    extension : "png",
                    title : "COMIC SHOP LOCATOR",
                    },
                    {
                    iconName : "dc-power-visa",
                    extension : "svg",
                    title : "DC POWER VISA",
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

img {
    width:  60px;
    height: 60px;
    object-fit: contain;
} 

span {
    color: $white;
    padding: 0.3rem;
    font-size: 14px;
}
}

</style>