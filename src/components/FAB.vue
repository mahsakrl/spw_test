<template>
  <div class="fab">
    <div class="fab-action-button-two">
      <p>
        By browsing this website, you consent to our
        <a href>Privacy Policy__</a>
        <a href>I agree</a>
      </p>
    </div>
    <div class="fab-action-button">
      <i
     
        class="fab-action-button__icon material-icons"
        style="cursor:pointer"
      >mode_comment</i>
    </div>
    <div class="fab-chat">
      <ChatCom />
    </div>
  </div>
</template>

<script>
import ChatCom from './Chat'
export default {
  data: () => {
    return {
      showChat: false
    }
  },


  components: {
    ChatCom
  },

}
</script>

<style>
body {
  font-family: Arial, sans-serif;
}
p {
  color: rgba(20, 20, 20, 0.64);
  text-align: center;
}
.fab {
  /* position:absolute;  */
  /* width: 56px; */
  /* left: 50%; */
  display: flex;
  align-items: center;
  justify-content: center;
  right: 5%;
  bottom: 15px;
  /* margin-left: -28px; */
}

 .fab:hover .fab-chat {
  opacity: 1;
  visibility: visible;
}

.fab:hover .fab-chat__link {
  transform: scaleY(1) scaleX(1) translateY(-16px) translateX(0px);
}

/* .fab-action-button:hover + .fab-chat .fab-chat__link:before {
  visibility: visible;
  opacity: 1;
  transform: scale(1);
  transform-origin: right center 0;
  transition-delay: 0.3s;
} */

.fab-action-button {
  /* position: absolute; */
  margin-right: 10px;
  margin-left: 200px;
  bottom: 0;
  display: block;
  width: 56px;
  height: 56px;
  background-color: rgb(98, 77, 227);
  border-radius: 50%;
  box-shadow: 0 2px 2px 0 rgba(0, 0, 0, 0.14), 0 1px 5px 0 rgba(0, 0, 0, 0.12),
    0 3px 1px -2px rgba(0, 0, 0, 0.2);
}
.fab-action-button-two {
  /* position: absolute; */
  /* margin-right:600px; */
  bottom: 0;
  display: block;
  width: 700px;
  height: 56px;
  background-color: white;
  border-radius: 56px;
  box-shadow: 0 2px 2px 0 rgba(0, 0, 0, 0.14), 0 1px 5px 0 rgba(0, 0, 0, 0.12),
    0 3px 1px -2px rgba(0, 0, 0, 0.2);
}

.fab-chat {
  position: absolute;
  left: 0;
  right: 0;
  bottom: 50px;
  list-style: none;
  margin: 0;
  padding: 0;
  opacity: 0;
  visibility: hidden;
  transition: 0.2s;
}

.fab-action-button__icon {
  display: inline-block;
  width: 56px;
  height: 56px;
  color: white;
  display: flex;
  align-items: center;
  justify-content: center; /* background: ("../assets/baseline_mode_comment_black_18dp.png") center no-repeat; */
}

.fab-chat__item {
  display: block;
  text-align: center;
  margin: 12px 0;
}

.fab-chat__link {
  display: inline-block;
  width: 40px;
  height: 40px;
  text-decoration: none;
  background-color: #ffffff;
  border-radius: 50%;
  box-shadow: 0 2px 2px 0 rgba(0, 0, 0, 0.14), 0 1px 5px 0 rgba(0, 0, 0, 0.12),
    0 3px 1px -2px rgba(0, 0, 0, 0.2);
  transform: scaleY(0.5) scaleX(0.5) translateY(0px) translateX(0px);
  -moz-transition: 0.3s;
  -webkit-transition: 0.3s;
  -o-transition: 0.3s;
  transition: 0.3s;
}

[data-tooltip]:before {
  top: 50%;
  margin-top: -11px;
  font-weight: 600;
  border-radius: 2px;
  background: #585858;
  color: #fff;
  content: attr(data-tooltip);
  font-size: 12px;
  text-decoration: none;
  visibility: hidden;
  opacity: 0;
  padding: 4px 7px;
  margin-right: 12px;
  position: absolute;
  transform: scale(0);
  right: 100%;
  white-space: nowrap;
  transform-origin: top right;
  transition: all 0.3s cubic-bezier(0.25, 0.8, 0.25, 1);
}

[data-tooltip]:hover:before {
  visibility: visible;
  opacity: 1;
  transform: scale(1);
  transform-origin: right center 0;
}

.icon-material {
  display: inline-block;
  width: 40px;
  height: 40px;
}
@media screen and (max-width:860px) {
  .fab-action-button-two {
  bottom: 0;
  margin-right: -50%;
  margin-left: -50%;
  display: block;
  width: 300px;
  height: 56px;
  background-color: white;
  border-radius: 56px;
  box-shadow: 0 2px 2px 0 rgba(0, 0, 0, 0.14), 0 1px 5px 0 rgba(0, 0, 0, 0.12),
    0 3px 1px -2px rgba(0, 0, 0, 0.2);
}
.fab-action-button {
  margin-right: -30%;
  bottom: 0;
  right: 0;
  /* display: block; */
  width: 56px;
  height: 56px;
  background-color: rgb(98, 77, 227);
  border-radius: 50%;
  box-shadow: 0 2px 2px 0 rgba(0, 0, 0, 0.14), 0 1px 5px 0 rgba(0, 0, 0, 0.12),
    0 3px 1px -2px rgba(0, 0, 0, 0.2);
}
}
</style>
