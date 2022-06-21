<template>
    <footer>
        <div class="container">
            <div class="row">
                <div class="col-4" v-for="link in footerLink" :key="link.nomeLink">
        
                
                    <h2>{{link.nomeLink}}</h2>
                    <ul>
                        <li v-for="(linkTest,i) in footerLink.link" :key="i">A</li>
                    </ul>
            
             
                </div>
                
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
                 nomeLink : "SHOP",
                 link :  ["Shop DC" , "Shop DC Collectibles"],
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
            ]
            }
        }
    }
</script>



<style lang="scss" scoped>
@import "../assets/style/main.scss";

footer {
    background-image: url("../assets/img/footer-bg.jpg");
    padding-top: 80px;
    padding-bottom: 100px;
    background-repeat: no-repeat;
    background-size: cover;
    color: #fff;
}



</style>