<template>
<div class="burger-wrapper">
  <div class="burger-men">
    <div>Features</div>
    <div>community</div>
  </div>
  <FAB  />
</div>
</template>

<script>
import FAB from "./FAB"
export default {
  components:{
    FAB
  }
}
</script>

<style>
.burger-wrapper{
  display:flex;
  align-items:center;
  justify-content:space-between;
  flex-flow:column;
  background-color:gray;
}
.burger-men {
  display: flex;
  flex-flow: column;
  z-index: 5000;
  margin-top: 100px;
}
</style>
