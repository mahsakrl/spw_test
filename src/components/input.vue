<template>
<div>
  <input type="text" placholder="your email">
  <input type="submit">
</div>
</template>

<script>
export default {

}
</script>

<style scoped lang="scss">
input[type="text"] {
    width: 200px;
    height: 80px;
    padding-right: 80px;
    border: 1px solid #C5AEC5;    
    border-radius:50px;
    outline: 0
}

input[type="submit"] {
    margin-left: -80px;
    height: 85px;
    width: 180px;
    background:#8E71DA;
    color: white;
    border: 0;
    -webkit-appearance: none;
    border-radius:50px;
}
</style>
