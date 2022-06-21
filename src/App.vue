<template>
  <div id="app">


    <TheNavBar/>
    <TheContent/>

  </div>
</template>

<script>
import TheNavBar from './components/TheNavBar.vue';
import TheContent from './components/TheContent.vue';


export default {
  name: 'App',
  components: {
    TheNavBar,
    TheContent
}
}
</script>

<style lang="scss">
</style>
