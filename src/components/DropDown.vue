<template>
  <div class="drop-wrapper">
    <div class="drop-row">
      <div class="drop-img"><img src="../assets/img/drop1.png" style="width:30%;height:70%"></div>
      <div class="drop-txt">Dynamic libraries</div>
    </div>
    <div class="drop-row">
      <div class="drop-img"><img src="../assets/img/drop1.png" style="width:30%;height:70%"></div>
      <div class="drop-txt">Dynamic libraries</div>
    </div>
  </div>
</template>

<script>
export default {

}
</script>

<style>
.drop-wrapper{
  width:300px;
  /* height:200px; */
  border-radius:20px;
  z-index: 5000;
  position: fixed;
  top:100px;
  right: 100px;
  display: flex;
  align-items: center;
  flex-flow: column;
  background-color: white;
}
.drop-row{
  display: flex;
  align-items: center;
  justify-content: center;
  border-bottom: 1px solid #f4f8fe;
  padding-bottom:20px; 
  padding-top:20px;
  padding-right:5px ; 
  padding-left:5px ; 
}
</style>
