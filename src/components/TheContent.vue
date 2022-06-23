<template>
<div>
  <div class="jumbotron">
  <img :src="currentBanner" alt="">
  </div>
  
  <div class="series pt-5 text-center">
    <div class="current-series">
      CURRENT SERIES
    </div>
    <div class="container p-4">
      <div class="row g-4">
        <div class="col-sm-6 col-md-4 col-lg-3 col-xl-2 " v-for="(comic,i) in comics" :key="comic.series" @click="getIndex(i)">
        <CardComic :imgUrl="comic.thumb" :id="i" :series="comic.series" :price="comic.price" :type="comic.type"></CardComic>
        </div>
      </div>
      
  </div>
  <button class="btn btn-primary text-light my-4">LOAD MORE</button>
</div>

</div>
</template>

<script>
import CardComic from './CardComic.vue';
    export default {
    name: "TheContent",
    components: { CardComic },

    data(){
        return{
            comics : [
  {
    "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/AC1000_DLX_162-001_HD_5ba13723281ab0.37845353.jpg?itok=ZsI-C5eX",
    "price": "$19.99",
    "series": "Action Comics",
    "type": "comic book",
    "jumbo" : "https://fumettologica.it/wp-content/uploads/2016/02/superman.jpg",
  },
  {
    "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/AV1976_01_300-001_HD_5f738f6e39ddd7.18205602.jpg?itok=VgdYdJ01",
    "price": "$3.99",
    "series": "American Vampire 1976",
    "type": "comic book",
    "jumbo" : "https://www.tomshw.it/images/images/2020/07/foto-generiche-104420.jpg",
  },
  {
    "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/gn-covers/2018/08/AQMv4_UW_153-001_HD_5b7efa1745a9b8.08589135.jpg?itok=HPTtnrsb",
    "price": "$16.99",
    "series": "Aquaman",
    "type": "graphic novel",
    "jumbo" : "https://www.staynerd.com/wp-content/uploads/aquaman-7.jpg",
  },
  {
    "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/06/batgirl_v5_1_5b23e1f1124941.50950783.jpg?itok=VnrJah76",
    "price": "$2.99",
    "series": "Batgirl",
    "type": "comic book",
    "jumbo" : "https://hotcorn-cdn.s3.amazonaws.com/wp-content/uploads/sites/2/2018/02/21124455/Batgirl-cinecomic-DC.jpg",
  },
  {
    "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/BM_56_300-001_HD_5ba137a85c3bf3.33122291.jpg?itok=3FHJQYJZ",
    "price": "$3.99",
    "series": "Batman",
    "type": "comic book",
    "jumbo" : "https://wallpaperaccess.com/full/1127064.jpg",
  },
  {
    "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/BM_56_300-001_HD_5ba137a85c3bf3.33122291.jpg?itok=3FHJQYJZ",
    "price": "$2.99",
    "series": "Batman Beyond",
    "type": "comic book",
    "jumbo" : "https://b-static.besthdwallpaper.com/batman-beyond-dc-comics-art-wallpaper-1366x768-90151_46.jpg",
  },
  {
    "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2019/08/BMSM_5d4361b7116261.74371456.jpg?itok=kEDR2OL8",
    "price": "$3.99",
    "series": "Batman/Superman",
    "type": "comic book",
    "jumbo" : "https://images2.alphacoders.com/623/623846.jpg",
  },
  {
    "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/BMSMANN_01_300-001_HD_5f5ff17fa1d665.74704970.jpg?itok=azz5sfGk",
    "price": "$4.99",
    "series": "Batman/Superman Annual",
    "type": "comic book",
    "jumbo" : "https://images2.alphacoders.com/657/657950.jpg",
  },
  {
    "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/BMTJWZ_01_300-001_HD_5f5ff2307dcb37.34652945.jpg?itok=VswVjLR8",
    "price": "$5.99",
    "series": "Batman: The Joker War Zone",
    "type": "comic book",
    "jumbo" : "https://cutewallpaper.org/22/hellbat-wallpapers/1256514682.jpg",
  },
  {
    "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/08/cover-v2_5f40314645a734.37285065.png?itok=ImNM2QBY",
    "price": "$6.99",
    "series": "Batman: Three Jokers",
    "type": "comic book",
    "jumbo" : "https://i.redd.it/xvuld1jlk6d51.png",
  },
  {
    "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/10/BMWK_HQ_01_300-001_HD_5f7cb4945e13f6.89501032.jpg?itok=sVwALbUX",
    "price": "$4.99",
    "series": "Batman: White Knight Presents: Harley Quinn",
    "type": "comic book",
    "jumbo" : "https://1.bp.blogspot.com/-V8YRE515nt4/X-KDyxlI3TI/AAAAAAAA2Ec/dvVPZwBKrOEixIAinyg0PGZTA-xHg8GegCLcBGAsYHQ/s1920/BWKP_HQ_Cv3_5fd28a81da6f49.07762789.jpg",
  },
  {
    "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/gn-covers/2019/04/CTWv1_CC_144-001_HD_5ca5299a751963.53054221.jpg?itok=ooPaoLDq",
    "price": "$16.99",
    "series": "Catwoman",
    "type": "graphic novel",
    "jumbo" : "https://wallpaperaccess.com/full/5398954.jpg",
  }
],
  
  currentBanner : require("../../public/img/jumbotron.jpg"),
  currentIndex : 0,
        }
    },

 methods: {

  getIndex : function(i){
    this.currentBanner = this.comics[i].jumbo;
  },

  cambiaImmagine : function(){
     this.currentBanner = this.comics[this.currentIndex].jumbo;
      this.currentIndex++;
       if(this.currentIndex>11)
  this.currentIndex=0;
  }
  
 },
 
created(){
  this.currentIndex = 0 ;
},

mounted(){
  setInterval(this.cambiaImmagine,1500);
}
    

    
}

</script>

<style lang="scss" scoped>
@import "../assets/style/main.scss";

.jumbotron {

    height: 600px;
    width: 100%;

  img {
    width: 100%;
    height: 100%;
    object-position: top right ;
    object-fit: cover;
  }

}


.series {
  background-color: $dark-black;
  position: relative;

  .current-series {position: absolute; color: $white; top: -3%; left: 15%; background-color: $light-blue; padding: 0.8rem 1.2rem; font-weight: bold;}
}

button {padding: 0.8rem 3.6rem; border-radius: 0; font-weight: bold;}

</style>