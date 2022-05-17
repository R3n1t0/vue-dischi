<template>
  <div class="container">

    <HeaderComp />
    <CardsComp />
  
  </div>
</template>

<script>
import CardsComp from './components/CardsComp.vue';
import HeaderComp from './components/HeaderComp.vue';


export default {
  name: 'App',
  components: {
    CardsComp,
    HeaderComp
}
}
</script>

<style lang="scss">
#app {
  
}
</style>
