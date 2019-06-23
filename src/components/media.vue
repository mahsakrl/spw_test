<template>
  <div class="media">
     <img src="../assets/img/5a615b4.png">
     <h3>
        {{title1}}
       <br>
       {{title2}}
     </h3>
     <p>{{subtitle}}</p>
  </div>
</template>

<script>
export default {
props:{
  img:String,
  title1:String,
  title2:String,
  subtitle:String
}
}
</script>

<style lang="scss" scoped>
.media{
  display: flex;
  align-items: center;
  justify-content: center;
  flex-flow: column
}
img{
  width:50%;
  height:50%
}
p{
  // color:#C5AEC5
}
</style>
