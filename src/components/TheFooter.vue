<template>
    <footer>
        <div class="container">
            <div class="row">
                <ul class="row">
                    <li class="col-4" v-for="item in footerLink" :key="item">
                        <h2>{{item.nomeLink}}</h2>
                        <p v-for="element in item.link" :key="element">
                        {{ element }}
                        </p>
                    </li>
                </ul>
                 
            </div>
        </div>
        <img class="logo-dc" src="../assets/img/dc-logo-bg.png" alt="">
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
    padding-top: 50px;
    padding-bottom: 50px;
    background-repeat: no-repeat;
    background-size: cover;
    color: #fff;
    position: relative;

.logo-dc {
    position: absolute;
    top: 50%;
    left: 80%;
    transform: translate(-50%, -50%);
    overflow: hidden;
    max-width: 100%;
    max-height: 100%;
 
}
}




</style>