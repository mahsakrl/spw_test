<template>
  <div class="logo-card">
    <i class="material-icons">{{icon}}</i>
    
  </div>
</template>

<script>
export default {
props:{
  icon:String
}
}
</script>

<style scoped lang="scss">
.logo-card{
  display: flex;
  align-items: center;
  justify-content: center;
  background-color: white;
  width:50px;
  height: 50px;
  border-radius: 16px;
  box-shadow: 2px 2px 0 2px #f4f8fe;
}
 
</style>
