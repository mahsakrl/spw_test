<template>
  <div class="app-wrapper">
    <div class="header">
      <div class="header-left">
        <LogoCom class="logo-com"/>
        <ButtonCom class="btn rounded secondary txt-color shadow btn-com" text="Coming 2019"/>
      </div>
      <div class="header-right" v-show="!burgerMenu">
        <DropDownCom v-show="activeDrop"/>
        <div class="header-menu">
          <div>Features</div>
          <i
            style="cursor:pointer"
            class="material-icons"
            @mouseover="activeDrop = true"
            @mouseleave="activeDrop = false"
            @click="activeDrop=!activeDrop"
          >keyboard_arrow_down</i>
        </div>
        <div class="community-title">Community</div>
      </div>
      <div class="burger" v-show="burgerMenu">
        <i class="material-icons" @click="showBurgerMenu=!showBurgerMenu">menu</i>
      </div>
      <BurgerMenuCom v-show="showBurgerMenu"/>
    </div>

    <div class="one">
      <HeaderCom
        class="title subtitle"
        title="All-in-one tool for design systems"
        subtitle="The first tool fully designed to maintain large products and design systems. All your design primitives, component states and platforms in one place."
      />
      <div class="inp-wrapper">
        <InputCom valueSub="Get early access" valueInp="Your email"/>
      </div>
      <img src="./assets/img/bg-one.png" alt style="width:100%;height:100%">
    </div>
    <div class="two">
      <HeaderCom
        class="title subtitle"
        title="A unified space for your daily work"
        subtitle="Specify provides all the tools needed to be ready to build the next generation of products software."
      />
      <!-- <div>
        <LogoCardCom class="logo-card" icon="face"></LogoCardCom>
        <LogoCardCom class="logo-card" icon="face"></LogoCardCom>
        <LogoCardCom class="logo-card" icon="face"></LogoCardCom>
        <LogoCardCom class="logo-card" icon="face"></LogoCardCom>
        <LogoCardCom class="logo-card" icon="face"></LogoCardCom>
        <LogoCardCom class="logo-card" icon="face"></LogoCardCom>
        <LogoCardCom class="logo-card" icon="face"></LogoCardCom>
        <LogoCardCom class="logo-card" icon="face"></LogoCardCom>
      </div> -->
    </div>
    <div class="three">
      <HeaderCom
        class="title subtitle"
        title="Specify is built for your company"
        subtitle="Make your product evolve coherently and scale your product teams at the right pace."
      ></HeaderCom>
      <div class="media-section">
        <div class="media-wrapper">
          <MediaCom
            title1="A bridge "
            title2="for product teams"
            subtitle="Your entire company is going to speak the same language by accessing the only source of truth you created."
            :img="mediaImg.one"
          />
          <MediaCom
            title1="Speed up"
            title2=" daily production"
            subtitle="Gain hours of work maintaining your code and reduce product debt. Say hello to a new kind of team velocity."
            :img="mediaImg.two"
          />
        </div>
        <div class="media-wrapper">
          <MediaCom
            title1="Brand"
            title2="Consistency"
            subtitle="Specify helps you keep the same identity across all the platforms you use. Increase your incomes and speed-up your time to market."
            :img="mediaImg.three"
          />
          <MediaCom
            title1="Facilitate"
            title2=" team scaling"
            subtitle="Every resources to start with are in Specify. Spend less time to onboard new co-workers. Start working faster and focus on what matters: users."
            :img="mediaImg.four"
          />
        </div>
      </div>
    </div>
    <div class="four">
      <HeaderCom
        class="title subtitle"
        title="Ready for your workflow"
        subtitle="Specify can be plugged to several services from design to development. Allowing you to shape it to your own workflow."
      ></HeaderCom>
      <div class="cards">
        <CardCom title="Multi OS"/>
        <CardCom title="Compatibility"/>
        <cardCom title="integrations"/>
      </div>
    </div>
    <div class="five">
      <HeaderCom
        class="title subtitle"
        title="Get early access"
        subtitle="Be the first to experience Specify before it’s publically available. Early beta will only be available for macOS."
      ></HeaderCom>
      <InputCom class="inp-wrapper" valueSub="Get early access" valueInp="Your email"/>
    </div>
    <div class="footer">
      <div class="footer-item">
        <LogoCom/>
        <p style="font-size:15px;color:rgba(20,20,20,0.64)">
          © Copyright 2019 Specify
          <br>All rights reserved
        </p>
        <div style="display:flex;align-items:center;justify-content:flex-start;margin-top:5px">
          <i class="material-icons" style="margin-right:10px">face</i>
          <i class="material-icons" style="margin-right:10px">pets</i>
          <i class="material-icons" style="margin-right:10px">today</i>
        </div>
      </div>
      <FooterCom class="footer-com" title="Features" :subtitle="subFeature"/>
      <FooterCom class="footer-com" title="Community" :subtitle="subCommunity"/>
      <FooterCom class="footer-com" title="Legal" :subtitle="subLegal"/>
    </div>
    <FAB chat/>
  </div>
</template>
<script>
import ButtonCom from './components/Button'
import HeaderCom from './components/Header'
import MediaCom from './components/Media'
import CardCom from './components/Card.vue'
import InputCom from './components/Input'
import FooterCom from './components/Footer'
import LogoCom from './components/LogoCom'
import FAB from './components/FAB'
import DropDownCom from './components/DropDown'
import LogoCardCom from './components/LogoCard'
import BurgerMenuCom from './components/BurgerMenu'
export default {
  data: () => {
    return {
      mediaImg: {
        one: require('./assets/img/1db079d.png'),
        two: require('./assets/img/5a615b4.png'),
        three: require('./assets/img/79c8646.png'),
        four: require('./assets/img/95c1a1c.png')
      },
      subFeature: {
        one: 'Dynamic Libraries',
        two: 'Continuous Delivery System',
        three: 'Atomic Hand-off'
      },
      subCommunity: {
        one: 'Facebook',
        two: 'Slack',
        three: 'Spectrum'
      },
      subLegal: {
        one: 'Privacy policy',
        two: 'Terms and services',
        three: 'contact'
      },
      activeDrop: false,
      burgerMenu: false,
      showBurgerMenu: false
    }
  },
  components: {
    ButtonCom,
    HeaderCom,
    MediaCom,
    CardCom,
    InputCom,
    FooterCom,
    LogoCom,
    FAB,
    LogoCardCom,
    DropDownCom,
    BurgerMenuCom
  },
  created() {
    window.addEventListener('resize', this.handleResize)
  },
  destroyed() {
    window.removeEventListener('resize', this.handleResize)
  },
  methods: {
    handleResize() {
      if (window.outerWidth < 600) this.burgerMenu = true
      else this.burgerMenu = false
    }
  }
}
</script>

<style lang="scss" scoped>
.app-wrapper {
  width: 100%;
  height: 100vh;
}
.header {
  width: 100%;
  height: 152px;
  display: flex;
  align-items: center;
  justify-content: space-between;
  background-color: #f4f8fe;
}
.header-left {
  display: flex;
  align-items: center;
  justify-content: flex-start;
 
  div {
    padding-right: 10px;
  }
}
.logo-com {
  padding-left: 55px;
}

.btn-com {
  margin-left: -10px;
   padding-right: 15px;
    // background-color: aqua
}
.header-right {
  display: flex;
  align-items: center;
  justify-content: flex-end;
  // background-color: aqua;
  margin-right: 30px;
  div {
    padding-right: 10px;
  }
}
.burger {
  margin-right: 30px;
}
.header-menu {
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding-right: 55px;
  // background-color: blue;
  margin-right: 40px;
  font-size:15px;
  // color:gray;
i{
  margin-left: -10px;
  margin-top:4px
};

}
.header-menu:hover{
  color:cadetblue
}
.community-title{
  font-size:15px;
}
.community-title:hover{
  color:cadetblue

}
///////////one

.one {
  width: 100%;
  background-color: #f4f8fe;
}

.inp-wrapper {
  display: flex;
  align-items: center;
  justify-content: center;
}

//////////////two

.two {
  width: 100%;
  display: flex;
  flex-flow: column;
  align-items: center;
  justify-content: center;
  div {
    display: flex;
    align-items: center;
    justify-content: center;
  }
}
.logo-card {
  margin: 20px;
}
/////////three

.three {
  width: 100%;
}
.media-section {
  display: flex;
  flex-flow: column;
  align-items: center;
  justify-content: center;
}
.media-wrapper {
  display: flex;
  align-items: center;
  justify-content: space-around;
}

//////four
.four {
  width: 100%;
}
.cards {
  display: flex;
  align-items: center;
  justify-content: center;
}
////five

.five {
  width: 100%;
  background-color: #f4f8fe;
}

.footer {
  width: 100%;
  // background-color: #f4f8fe;
  display: flex;
  align-items: flex-start;
  justify-content: space-around;
}
.footer-item {
  display: flex;
  flex-flow: column;
  padding-top: 40px;
}
.footer-com{
  display: flex;
  align-items: center;
  justify-content: center
}
@media screen and (max-width: 850px) {
  .media-wrapper {
    display: flex;
    align-items: center;
    flex-flow: column;
    justify-content: space-around;
  }
  .cards {
    display: flex;
    align-items: center;
    justify-content: center;
    flex-flow: column;
  }
   .footer {
    width: 100%;
    //  background-color: #f4f8fe;
    display: flex;
    flex-flow: column;
    align-items: flex-start;
    justify-content: flex-start;
    p {
      display: none;
    }
    i {
      display: none;
    }
  }
  .footer-item {
    display: flex;
    flex-flow: column;
    padding-top: 40px;
    width: 100%;
    align-items: center;
  }
  .footer-com{
  display: flex;
  align-items: center;
  justify-content: center
}
}
@media screen and (max-width: 620px) {
  .header-right {
    display: none;
  }
 
}
</style>
