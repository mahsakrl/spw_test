<template>
  <div class="chat">
    <div class="chat-header">
      <i v-show="inChat" class="material-icons" v-on:click="inChat=false">keyboard_arrow_left</i>
      <div class="header-container">
        <h4 v-show="inChat">specify</h4>
        <img
          style="width:10%;height:10%;margin-left:30px;margin-top:30px"
          src="https://specifyapp.com/favicon.ico"
          v-show="!inChat"
        >
        <h4 v-show="!inChat" style="margin-left:30px">Hi There</h4>
        <p style="margin-left:30px">Ask us anything, or share your feedback.</p>
        <!-- <div v-show="!inChat" class="chat-start" style="position:absolute;bottom:50%">1</div> -->

        <div v-show="inChat" class="chat-img">
          <div>
            <img src="../assets/img/chat_img1.png">
            <p>louis</p>
          </div>
          <div>
            <img src="../assets/img/chat_img2.png">
            <p>prrer</p>
          </div>
        </div>
        <p v-show="inChat" style="margin-top:30px">back in 1h</p>
      </div>
    </div>
    <div style="position:absolute;bottom:50%;margin:5px;" v-show="!inChat" class="chat-start">19</div>

    <div class="chat-main">
      <p style="font-size:10px">we run on InterCom</p>
    </div>
    <div v-show="inChat" class="chat-input">
      <input placeholder="send message...">
    </div>
  </div>
</template>

<script>
export default {
  data: () => {
    return {
      inChat: true
    }
  }
}
</script>

<style scoped lang="scss">
img {
  width: 100%;
  height: 100%;
  border-radius: 50%;
}
.chat-img {
  width: 100%;
  display: flex;
  align-items: center;
  justify-content: flex-start;
  div {
    width: 50px;
    height: 50px;
    border-radius: 25px;
    background-color: aliceblue;
    display: flex;
    align-items: center;
    flex-flow: column;
    justify-content: flex-start;
    margin-right: 15px;
  }
}
.chat {
  width: 300px;
  height: 400px;
  background-color: white;
  display: flex;
  flex-flow: column;
  align-items: center;
  justify-content: flex-start;
  position: absolute;
  right: 56px;
  bottom: 5px;
}
.chat-start {
  background-color: aqua;
  height: 40px;
  width: 100%;
  z-index: 1000;
  align-self: flex-end;
}

.chat-header {
  width: 100%;
  height: 200px;
  background-color: #624de3;
  display: flex;
  align-items: flex-start;
  justify-content: flex-start;
}
.header-container {
  display: flex;
  flex-flow: column;
  flex-grow: 5;
  align-items: flex-start;
  justify-content: flex-start;
  h4 {
    color: white;
    margin: 0;
    margin-top: 20px;
  }
  p {
    color: rgba(255, 255, 255, 0.7);
    font-size: 10px;
  }
  // margin-left: 15px;
  // background-color: aqua
}
i {
  flex-grow: 2;
  margin-top: 20px;
  margin-left: 15px;
  color: white;
}
.chat-main {
  width: 100%;
  flex-grow: 5;
  background-color: white;
  display: flex;
  align-items: center;
  justify-content: center;
  overflow: auto;
  p {
    color: #777678;
  }
}
.chat-input {
  width: 100%;
  flex-grow: 1;
  background-color: white;
  input {
    width: 100%;
    height: 30px;
    outline: 0;
    border: none;
    border-top: 1px solid #f4f8fe;
    background: url('../assets/img/baseline_attach_file_black_18dp.png')
      no-repeat right 5% bottom 5%;
    padding-left: 15px;
    padding-top: 15px;
  }
}
</style>
