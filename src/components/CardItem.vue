<template>
  <div class="d-flex text-center p-3 m-2">
    <img :src="cardData.poster" :alt="cardData.author">
    <h6>{{cardData.title}}</h6>
    <p>{{cardData.author}}</p>
    <span>{{cardData.year}}</span>
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
div{
  flex-basis: calc(100% / 6);
  flex-direction: column;
  align-items: center;
  background-color: #2e3a46;
  img{
    width: 100%;
    height: 60%;
  }
  h6{
    color: white;
    margin-top: 20px;
  }
  
}

</style>