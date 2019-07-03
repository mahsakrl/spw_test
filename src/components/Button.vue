<template>
  <div class="btn">
    <p class="btn-txt">{{text}}</p>
  </div>
</template>

<script>
export default {
  props: {
    text: String
  }
}
</script>

<style <style lang="scss" scoped>
.btn {
  width: 100px;
  height: 30px;
  background-color: #454ccd;
  color: white;
  cursor: pointer;
  display: flex;
  align-items: center;
  justify-content: center;
}
.rounded {
  border-radius: 20px;
}
.shadow {
  box-shadow: 0 12px 16px 0 rgba(237, 242, 251, 0.71);
}
.secondary {
  background-color: white;
  &.txt-color {
    .btn-txt {
      color: rgba(20, 20, 20, 0.64);
      font-size: 14px;
      font-family: 'Eina 02-bold', sans-serif;
      font-weight: bold;
      text-align: center

    }
  }
  &.lg {
    width: 200px;
    height: 200px;
    border-radius: 10px;
  }
}
</style>

