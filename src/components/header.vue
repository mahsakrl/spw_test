<template>
  <div classs="section-header">
    <h1 class="title">{{title}}</h1>
    <p class="subtitle">{{subtitle}}</p>
  </div>
</template>

<script>
export default {
props:{
  title:String,
  subtitle:String
}
}
</script>

<style lang="scss" scoped>
.section-header{
  display:flex;
  align-items: center;
  justify-content: center;
  width:200px;
  &.title{
div {
  color:violet
}
  };

}
p{
  color:rgba(20, 20, 20, 0.64);
  font-size: 25px;
  font-display: "Roboto-Regular,sans-serif"
}
</style>
