<template>
  <div>

    <div class="container-fluid">
      <HeaderComp />
    </div>
    
    <div class="container">
      <CardsComp />
    </div>
    
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

</style>
