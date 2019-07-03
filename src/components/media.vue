<template>
  <div class="media">
    <img :src="img" style="width:40%">
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
  props: {
    img: String,
    title1: String,
    title2: String,
    subtitle: String
  }
}
</script>

<style lang="scss" scoped>
.media {
  display: flex;
  align-items: center;
  justify-content: center;
  flex-flow: column;
  p {
  font-family: sans-serif;
  color: rgba(20, 20, 20, 0.64);
  font-size: 24px;
  font-style: normal;
  text-align: center;
  width: 500px;
};
h3 {
  font-family: sans-serif;
  font-size: 40px;
  font-style: normal;
  text-align: center
}
}
@media screen and (max-width:850px) {
  .media {
     p {
  font-family: sans-serif;
  color: rgba(20, 20, 20, 0.64);
  width:50%;
  font-size: 20px;
  font-style: normal;
  text-align: center
};
h3 {
  font-family: sans-serif;
  font-size: 30px;
  width:50%;
  font-style: normal;
  text-align: center
}
  }
}



</style>
