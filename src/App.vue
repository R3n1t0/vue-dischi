<template>
  <div>   
    <CardsComp class="native" />            
  </div>
</template>

<script>
import CardsComp from './components/CardsComp.vue';

export default {
  name: 'App',
  components: {
    CardsComp,
  }
}
</script>

<style lang="scss">
@import './assets/style/general';
@import './assets/style/vars';


</style>
