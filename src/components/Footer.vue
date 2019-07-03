<template>
  <div class="footer-com">
     <div class="h4" @click="footer=!footer">
      <div>  {{title}}</div>
        <i class="material-icons" v-show="!footer">keyboard_arrow_down</i>
        <i class="material-icons" v-show="footer">keyboard_arrow_up</i>
      </div>
    <div class="ul-class">
     
      <div class="li-class" v-show="footer" v-for="(item,index) in subtitle" :key="index">{{item}}</div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    title: String,
    subtitle: Object
  },
  data: () => {
    return {
      footer: false
    }
  }
}
</script>

<style scoped lang="scss">
.footer-com {
  display: flex;
  height:600px;
  align-items: flex-start;
  justify-content: flex-start;
  flex-flow: column
  // padding-bottom: 130px;
}
i {
  display: none;
}
.ul-class {
  list-style: none;
}
.li-class {
  text-align: left;
  font-size: 15px;
  color: rgba(20, 20, 20, 0.64);
  padding-top: 8px;
}
.h4 {
  font-size: 20px;
  display: flex;
  align-items: center;
  justify-content: space-between
}

@media screen and (max-width: 850px) {
  i {
    display: inline;
  }
  .footer-com {
    display: flex;
    flex-flow: column;
    justify-content: center;
    align-items: center;
    width:100%;
    // background-color: aqua;
  }
  .h4 {
    min-width: 100%;
    font-size: 20px;
    display: flex;
    align-items: center;
    justify-content: space-between;
    // background-color: blue
  }
  .ul-class {
   text-align: left;
  
  }
  .li-class{
    font-size: 15px;
    // background-color: red;
    width:100%;
    margin-left: -90%
  }
}
</style>
