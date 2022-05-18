<template>
  <div class="cards d-flex">
    <CardItem 
      v-for="card in cardsList.response"
      :key="`card-${card}`"
      :cardData="card"
    />
  </div>
</template>

<script>
import axios from "axios"
import CardItem from "./CardItem.vue"


export default {
  name: "CardsComp",
  data(){
    return{
      apiUrl: "https://flynn.boolean.careers/exercises/api/array/music",
      cardsList: [],
    };
  },

  mounted(){
    this.getApi();
  },

  methods:{
    getApi(){
      axios.get(this.apiUrl)
      .then(res => {
        this.cardsList = res.data;
      });
    },
  },

  components:{
    CardItem
  }
}
</script>

<style lang="scss" scoped>

.cards{
  width: 100%;
}

</style>