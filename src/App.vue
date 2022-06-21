<template>
  <div id="app">


    <TheNavBar/>
    <TheContent/>
    <IconBanner/>
    <TheFooter/>
    <SignUp/>
  </div>
</template>

<script>
import TheNavBar from './components/TheNavBar.vue';
import TheContent from './components/TheContent.vue';
import IconBanner from './components/IconBanner.vue';
import TheFooter from './components/TheFooter.vue';
import SignUp from './components/SignUp.vue';


export default {
  name: 'App',
  components: {
    TheNavBar,
    TheContent,
    IconBanner,
    TheFooter,
    SignUp
}
}
</script>

<style lang="scss">
</style>
