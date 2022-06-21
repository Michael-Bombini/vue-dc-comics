<template>
  <div id="app">


    <TheNavBar/>
    <TheContent/>
    <IconBanner/>
    <TheFooter/>
  </div>
</template>

<script>
import TheNavBar from './components/TheNavBar.vue';
import TheContent from './components/TheContent.vue';
import IconBanner from './components/IconBanner.vue';
import TheFooter from './components/TheFooter.vue';


export default {
  name: 'App',
  components: {
    TheNavBar,
    TheContent,
    IconBanner,
    TheFooter
}
}
</script>

<style lang="scss">
</style>
