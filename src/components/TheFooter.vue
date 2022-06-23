<template>
    <footer>
        <div class="container d-flex">
            <div class="row col-6">
                <ul class="row">
                    <li class="col-4" v-for="item in footerLink" :key="item.nomeLink">
                        <h2 class="py-3">{{item.nomeLink}}</h2>
                        <p v-for="element in item.link" :key="element">
                        {{ element }}
                        </p>
                    </li>
                </ul>
                 
            </div>
            <div class="h-100">
                <img class="logo-dc" src="../assets/img/dc-logo-bg.png" alt="">
            </div>
        </div>
    
    </footer>
</template>

<script>
    export default {
        name : "TheFooter",
        data(){
            return{
                footerLink : [
                {
                 nomeLink : "DC COMICS",
                 link : ["Character" , "Comics" , "Movies" , "TV" , "Games" , "Videos" , "News"],
                },
                {

                      nomeLink : "DC",
                 link : ["Terms Of Use" , "Privacy Policy (New)" , "Ad Choices" , "Advertising" , "Jobs" , "Subscriptions" , 
                        "Talent Workshops" , "CPSC Certificates" , "Ratings" , "Shop Help" , "Contact Us"],

                },
                {
                     nomeLink : "SITES",
                 link : ["DC" , "MAD Magazine" , "DC Kids" , "DC Universe" , "DC Power Visa"],

                },
                {
                    nomeLink : "SHOP",
                 link :  ["Shop DC" , "Shop DC Collectibles"],
                },
            ]
            }
        }
    }
</script>



<style lang="scss" scoped>
@import "../assets/style/main.scss";

footer {
    background-image: url("../assets/img/footer-bg.jpg");
    padding-top: 25px;
    padding-bottom: 25px;
    background-repeat: no-repeat;
    background-size: cover;
    color: #fff;
    position: relative;

.logo-dc {
    width: 100%;
 
}

p {
    color: darken($white , 40%);
}

}

div.h-100 {
    position: absolute;
    top: 50%;
    left: 70%;
    transform: translate(-50%, -50%);
    overflow: hidden;
}


</style>