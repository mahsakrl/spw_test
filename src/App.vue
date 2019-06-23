<template>
  <div id="app">
    <div class="header">
      <div class="header-left">
        <div class="header-logo">
          <img src="./assets/logo.png" style="width:32px;height:32px">
        </div>

        <div class="header-txt">Specify</div>

        <buttonCom class="btn rounded secondary txt-color shadow" text="Coming 2019"></buttonCom>
      </div>
      <div class="header-right">
        <div style="display:flex;align-items:center">
          <div>Features</div>
          <i class="material-icons">keyboard_arrow_down</i>
        </div>
        <div>Community</div>
      </div>
    </div>
    <div class="one">
      <headerCom
      class="title subtitle"
        title="All-in-one tool for design systems"
        subtitle="The first tool fully designed to maintain large products and design systems. All your design primitives, component states and platforms in one place."
      ></headerCom>
      <div style="display:flex;align-items:cenetr;justify-content:center">
      <inputCom />
        <!-- <buttonCom class="rounded lg" text="Get early access"></buttonCom> -->
      </div>
      <img src="./assets/img/bg-one.png" alt style="width:100%;height:100%">
    </div>
    <div class="two">
       <headerCom
      class="title subtitle"
        title="A unified space for your daily work"
        subtitle="Specify provides all the tools needed to be ready to build the next generation of products software."
      ></headerCom>
    </div>
    <div class="three">
       <headerCom
      class="title subtitle"
        title="Specify is built for your company"
        subtitle="Make your product evolve coherently and scale your product teams at the right pace."
      ></headerCom>
      <div class="media-section">
        <div style="display:flex;align-items:center;justify-content:space-between" >
        <mediaCom style="width:20%" title1="A bridge " title2="for product teams" subtitle="Your entire company is going to speak the same language by accessing the only source of truth you created." img="./assets/img/1db079d.png" />
        <mediaCom style="width:20%" title1="Speed up" title2=" daily production" subtitle="Gain hours of work maintaining your code and reduce product debt. Say hello to a new kind of team velocity." img='./assets/img/5a615b4.png' />
        </div>
        <div style="display:flex;align-items:center;justify-content:space-between">
        <mediaCom style="width:20%" title1="Brand" title2="Consistency" subtitle="Specify helps you keep the same identity across all the platforms you use. Increase your incomes and speed-up your time to market." img='./assets/img/79c8646.png' />
        <mediaCom style="width:20%" title1="Facilitate " title2=" team scaling" subtitle="Every resources to start with are in Specify. Spend less time to onboard new co-workers. Start working faster and focus on what matters: users." img='./assets/img/95c1a1c.png' />
        </div>
      </div>
    </div>
    <div class="four">
       <headerCom
      class="title subtitle"
        title="Ready for your workflow"
        subtitle="Specify can be plugged to several services from design to development. Allowing you to shape it to your own workflow."
      ></headerCom>
      <div class="cards">
      <cardCom title="Multi OS"></cardCom>
      <cardCom title="Compatibility">
        <ul>
          <li>
            <i class="material-icons"></i>
          </li>
          <li>
            <i class="material-icons"></i>

          </li>
          <li>
            <i class="material-icons">xd</i>

          </li>
        </ul>
      </cardCom>
      <cardCom title="integrations"></cardCom>
      </div>

    </div>
    <div class="five">
       <headerCom
      class="title subtitle"
        title="Get early access"
        subtitle="Be the first to experience Specify before it’s publically available. Early beta will only be available for macOS."
      ></headerCom>
      <inputCom />
    </div>
    <div class="footer"></div>
  </div>
</template>
<script>
import buttonCom from './components/Button'
import headerCom from './components/header'
import mediaCom from "./components/media"
import cardCom from "./components/card.vue"
import inputCom from "./components/input"
export default {
  components: {
    buttonCom,
    headerCom,
    mediaCom,
    cardCom,
    inputCom
  }
}
</script>

<style lang="scss" scoped>
#app {
  // font-family: 'Avenir', Helvetica, Arial, sans-serif;
  font-family: 'Eina 02-bold', sans-serif;
  text-align: center;
  // color: #2c3e50;

}
input{
  width:100px;
  height:50px;
  border-radius: 10px;
  background: url('./assets/logo.png') no-repeat 10px 10px;

}
.header {
  width: 100%;
  height: 152px;
  background-color: white;
  display: flex;
  align-items: center;
  justify-content: space-between;
}
.header-right {
  width: 500px;
  height: 50px;
  // background-color: violet;
  display: flex;
  align-items: center;
  justify-content: flex-end;
  div {
    padding-right: 10px;
  }
}
.header-left {
  width: 500px;
  height: 50px;
  // background-color: aqua;
  display: flex;
  align-items: center;
  justify-content: flex-start;
  .buttonCom {
    padding-right: 10px;
  }
  div {
    padding-right: 10px;
  }
}
.one {
  width: 100%;
  // height: 900px;
  // background-color: navajowhite;
}
.two {
  width: 100%;
  // height: 200px;
  // background-color: mediumaquamarine;
}
.three {
  width: 100%;
  // height: 800px;
  // background-color: moccasin;
}
.media-section{
  display: flex;
  flex-flow: column;
  align-items: center;
  justify-content: center

}
.four {
  width: 100%;
  // height: 600px;
  // background-color: navy;
}
.cards{
  display: flex;
  align-items: center;
  justify-content: center;
}
.footer {
  width: 100%;
  height: 200px;
  background-color: rosybrown;
}
</style>
