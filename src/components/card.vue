<template>
  <div class="card">
    <h3>{{title}}</h3>

    <div style="social-card">
      <i class="material-icons">face</i>
      
       <!-- <svg style="width:50px;height:50px;background-color:red"><a href="https://specifyapp.com/_nuxt/icons.svg"></a></svg> -->
       <!-- <img src="https://specifyapp.com/favicon.ico"> -->
      <i class="material-icons">pets</i>
      <i class="material-icons">today</i>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    title: String,
    icon1: Array,
    icon1: Array
  }
}
</script>

<style lang="scss" scoped>
.card {
  width: 300px;
  height: 200px;
  border-radius: 20px;
  background-color: #f4f8fe;
  margin: 40px;
  display: flex;
  align-items: center;
  justify-content: center;
  flex-flow: column;
}

.social-card {
  display: flex;
  align-items: center;
  justify-content: center;
}
i {
  margin: 20px;
}
@media screen and (max-width:850px) {
  .card{
    width:100%;
    height:300px;
    h3{
  font-size: 30px
}
  }
  
i {
  margin: 20px;
  font-size: 50px
}

}
</style>
