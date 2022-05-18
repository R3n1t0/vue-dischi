<template>
  <div>

    <div class="container-fluid d-flex align-items-center">
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
@import './assets/style/general';
@import './assets/style/vars';

.container-fluid{
  height: 60px;
  background-color: #2b343f;
}
</style>
