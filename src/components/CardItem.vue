<template>
  <div>
    <img :src="cardData.poster" :alt="cardData.author">
    <h4>{{cardData.title}}</h4>
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
  width: calc(100% / 5);
  img{
    width: 100%;
  }
}

</style>