<template>

  <div class="rl-container">

    <div class="top">
      <SelectComp @searching="searching"/>
    </div>

    <div class="cards-container d-flex mt-5 container">
      <CardItem 
      :genreChosed="genreChosed"
      v-for="(card, index) in cardsList"
      :key="`card-${index}`"
      :cardData="card"
      />
    </div>
    
  </div>
  
</template>

<script>
import axios from "axios"
import CardItem from "./CardItem.vue"
import SelectComp from "./SelectComp.vue";


export default {
  name: "CardsComp",
  data(){
    return{
      apiUrl: "https://flynn.boolean.careers/exercises/api/array/music",
      cardsList: [],
      genreChosed: ""
    };
  },

  mounted(){
    this.getApi();
  },

  methods:{
    getApi(){
      axios.get(this.apiUrl)
      .then(res => {
        this.cardsList = res.data.response;
      });
    },

    searching(genreChosed){
      this.genreChosed = genreChosed
    }
  },

  components:{
    CardItem,
    SelectComp
  }
}
</script>

<style lang="scss" scoped>

.rl-container{
  width: 100%;
  height: 100vh;

  .top{
    width: 100%;
  }

  .cards-container{
    height: calc(100vh - 50px);
    justify-content: center;
    flex-wrap: wrap;
  }
}

</style>