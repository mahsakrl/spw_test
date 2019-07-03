<template>
  <div class="inp">
    <input type="text" :placeholder="valueInp">
    <input type="submit" :value="valueSub">
  </div>
</template>

<script>
export default {
  props: {
    valueSub: String,
    valueInp: String
  }
}
</script>

<style scoped lang="scss">
.inp{
  margin: 20px;

}
input[type='text'] {
  width: 200px;
  height:70px;
  padding-right: 80px;
  padding-left: 50px;
  border: 1px solid #c5aec5;
  font-size: 20px;
  font-weight: 200;
  border-radius: 50px;
  outline: 0;
}

input[type='submit'] {
  margin-left: -130px;
  height: 74px;
  // width: 160px;
  background: #624de3;
  color: white;
  font-size: 15px;
  font-weight: 700;
  border: 0;
  border-radius: 85px;
  outline: 0;
  padding-right:32px;
  padding-left:32px
}
@media screen and (max-width:850px) {
 
input[type='text'] {
  width: 200px;
  height: 52px;
   padding-right: 15px;
   padding-left: 15px;
  border: 1px solid #c5aec5;
  font-size: 14px;
  border-radius: 50px;
  outline: 0;
}

input[type='submit'] {
  margin-left: -70px;
  height: 55px;
  width: 100px;
  background: #624de3;
  color: white;
  font-size: 10px;
  border: 0;
  padding:10px;
  border-radius: 85px;
  outline: 0;
} 
}
</style>
