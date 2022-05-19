<template>
  <div class="rl-card d-flex text-center p-3 m-2">
    <img :src="cardData.poster" :alt="cardData.title">
    <h6>{{cardData.title}}</h6>
    <p>{{cardData.author}}</p>
    <p>{{cardData.year}}</p>
  </div>
</template>

<script>
export default {
  name: "CardItem",

  props:{
    cardData:Object
  }
}
</script>

<style lang="scss" scoped>
.rl-card{
  width: calc(100% / 6);
  height: 350px;
  flex-direction: column;
  align-items: center;
  background-color: #2e3a46;
  img{
    width: 100%;
  }
  h6{
    color: white;
    margin-top: 20px;
  }
  p{
    color: #787574;
  }
  
}

</style>