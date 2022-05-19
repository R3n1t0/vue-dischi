<template>

  <div class="rl-container">

    <div class="top">
      <SelectsComp @genreSearching="genreSearching" @albumSearching="albumSearching"/>
    </div>

    <div class="cards-container d-flex mt-5 container">
      <CardItem 
      v-for="(card, index) in genreFiltered"
      :key="`card-${index}`"
      :cardData="card"
      />
    </div>
    
  </div>
  
</template>

<script>
import axios from "axios"
import CardItem from "./CardItem.vue"
import SelectsComp from "./SelectsComp.vue";


export default {
  name: "CardsComp",

  components:{
    CardItem,
    SelectsComp
  },

  data(){
    return{
      apiUrl: "https://flynn.boolean.careers/exercises/api/array/music",
      cardsList: [],
      genreChosed: "",
      albumChosed: ""
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

    genreSearching(genreChosed){
      this.genreChosed = genreChosed
    },

    albumSearching(albumChosed){
      this.albumChosed = albumChosed
    }
  },

  computed:{
    genreFiltered(){
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