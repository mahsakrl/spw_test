<template>
  <div class="section-header">
    <div style="padding-right:64px;padding-left:64px;">
    <h1 class="title">{{title}}</h1>
    <p class="subtitle">{{subtitle}}</p>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    title: String,
    subtitle: String
  }
}
</script>

<style lang="scss" scoped>
.section-header {
  display: flex;
  flex-flow: column;
  align-items: center;
  justify-content: center;
 
  //  background-color: aqua;

  &.title {
    div {
      // color: violet;
    }
  }
  h1 {
  font-size: 60px;
  text-align: center;
  

};
p {
  color: rgba(20, 20, 20, 0.64);
  font-size: 27px;
  font-display: 'Roboto-Regular,sans-serif';
    width: 920px;
    line-height: 40px;
  text-align: justify center
}

}
@media screen and (max-width:850px) {
  .section-header{
 h1 {
  font-size: 35px;
  text-align: center;

};
p {
  color: rgba(20, 20, 20, 0.64);
  font-size: 20px;
  font-display: 'Roboto-Regular,sans-serif';
    width: 100%;
  text-align: justify center
}
}
}
</style>
