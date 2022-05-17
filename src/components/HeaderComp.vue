<template>
  <header class="d-flex space-between align-items-center">
    <i class="fa-brands fa-spotify"></i>
    <select class="form-select rl-select" name="generi" >
      <option selected>Seleziona un genere</option>
    </select>
  </header>
</template>

<script>
export default {
  name: "HeaderComp"
}
</script>

<style lang="scss" scoped>
@import "../assets/style/_vars.scss";
header{
  width: 100%;
  justify-content: space-between;
  
  i{
    color: #34be58;
    font-size: 30px;
  }
  
  .rl-select{
    width: 11%;
    border: none;
    padding: 5px 12px;
    border-radius: 5px;
    font-size: 12px;
  }
}



</style>