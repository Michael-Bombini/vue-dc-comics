<template>
  <div id="app">


    <TheNavBar/>
    <TheContent/>
    <IconBanner/>

  </div>
</template>

<script>
import TheNavBar from './components/TheNavBar.vue';
import TheContent from './components/TheContent.vue';
import IconBanner from './components/IconBanner.vue';


export default {
  name: 'App',
  components: {
    TheNavBar,
    TheContent,
    IconBanner
}
}
</script>

<style lang="scss">
</style>
