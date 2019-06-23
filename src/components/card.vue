<template>
  <div class="card">
    <h3>{{title}}</h3>
  <div v-for="(item,index) in icon" :key="index">
    <i class="material-icons">{{item.icon}}</i>
  </div>
  </div>
</template>

<script>
export default {
props:{
  title:String,
  icon1:Array,
  icon1:Array,
}
}
</script>

<style lang="scss" scoped>
.card{
  width:300px;
  height:200px;
  border-radius: 20px;
  background-color: #f4f8fe;
  margin:40px;
 
}

</style>
