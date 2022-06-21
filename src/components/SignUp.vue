<template>
    <div class="sign-up p-2">
        <div class="container d-flex justify-content-between py-3">
            <div>
                <button type="button" class="btn btn-outline-primary text-light p-3">SIGN UP NOW</button>
            </div>
            <div>
               <div class="d-flex gap-2">
                <h3>FOLLOW US</h3>
                <img src="../assets/img/footer-facebook.png" alt="" />
                <img src="../assets/img/footer-periscope.png" alt="" />
                <img src="../assets/img/footer-pinterest.png" alt="" />
                <img src="../assets/img/footer-twitter.png" alt="" />
                <img src="../assets/img/footer-youtube.png" alt="" />
            </div>
                
            </div>

        </div>
    </div>
</template>

<script>
    export default {
        name : "SignUp",
        data(){
            return{

            }
        }
    }
</script>

<style lang="scss" scoped>
@import "../assets/style/main.scss";
.sign-up {
    background-color: $light-black;


h3{
    color: $light-blue;
    text-transform: uppercase;
}
}


</style>