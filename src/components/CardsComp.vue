<template>

  <div class="rl-container">

    <div class="top">
      <SelectComp @searching="searching"/>
    </div>

    <div class="cards-container d-flex mt-5 container">
      <CardItem 
      v-for="(card, index) in arrayFiltered"
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

  components:{
    CardItem,
    SelectComp
  },

  data(){
    return{
      apiUrl: "https://flynn.boolean.careers/exercises/api/array/music",
      cardsList: [],
      genreChosed: "",
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

  computed:{
    arrayFiltered(){
      if(this.genreChosed === ""){
        return this.cardsList;
      }
      return this.cardsList.filter(album => album.genre === this.genreChosed) 
    }
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