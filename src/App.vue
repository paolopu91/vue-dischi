<template>
  <div>

    <TheHeader />
    

    <CentralMain />

  </div>
</template>

<script>
import TheHeader from './components/TheHeader.vue';
import CentralMain from './components/CentralMain.vue';




export default {
  name: 'App',
  components: {
    TheHeader,
    CentralMain,
    
  }
}
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
