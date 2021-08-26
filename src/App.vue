<template>
  <div id="app">
    <div class="container">
      <nav class="nav-menu">
        <NavIcon>
          <IconLogo/>
        </NavIcon>
        <NavIcon v-for="(item, iconIndex) in navMenu" :key="iconIndex"
          @click.native="iconClick(iconIndex)"
          :activeNav= item.isActive
        >
          <component :is ='item.icon'
            :activeIcon= item.isActive
          >
          </component>
        </NavIcon>
        <div class="nav-menu_text">relief arc</div>
      </nav>

      <div class="header-container">
        <div class="header">
          <Selector/>
          <div class="header__center"></div>
          <Profile/>
        </div>

        <div class="search-container">
          <Search class="search__input"/>
          <Switcher
            :items = switchIcons
          >
          </Switcher>
          <Info/>
          <SearchBtn
            title = "Involvement"
            image = "image/compass.png"
          >
          </SearchBtn>
          <SearchBtn
              title = "Configure Initiative"
          >
          </SearchBtn>
          <SearchBtn
              title = "New"
              image = "image/plus.png"
              color = "#FBBC05"
          >
          </SearchBtn>
        </div>

        <div class="search-setting">
          <Switcher
              :items = switchText
              :padding = '"12px 78px 12px 78px"'
          >
          </Switcher>
          <div class="search-setting__slider">
            <img src="image/setting.png" alt="">
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import NavIcon from '@/components/NavIcon.vue';
import Selector from '@/components/Selector.vue';
import Profile from '@/components/Profile.vue';
import Switcher from '@/components/Switcher.vue'
import Search from '@/components/Search.vue'
import Info from '@/components/Info.vue'
import SearchBtn from '@/components/SearchBtn.vue'

import IconHome from "@/components/svg/nav_icon/IconHome";
import IconCube from "@/components/svg/nav_icon/IconCube";
import IconLogo from "@/components/svg/nav_icon/IconLogo";
import IconUser from "@/components/svg/nav_icon/IconUser";
import IconStat from "@/components/svg/nav_icon/IconStat";
import IconEarth from "@/components/svg/header_icon/IconEarth";
import IconLocation from "@/components/svg/header_icon/IconLocation";

export default {
  name: 'App',
  components: {
    Selector,
    NavIcon,
    Profile,
    Switcher,
    Search,
    Info,
    SearchBtn,

    IconLogo,
   /* IconCube,
    IconHome,
    IconUser,
    IconStat,*/
  },

  data: function () {
    return {
      activeNav: 0,

      navMenu: [
        {
          icon: IconHome,
          isActive: true,
        },
        {
          icon: IconUser,
          isActive: false,
        },
        {
          icon: IconCube,
          isActive: false,
        },
        {
          icon: IconStat,
          isActive: false,
        }
      ],
      yellow: '#FBBC05',
      black: '#2D2D2D',

      switchIcons: [
        {
          icon: IconEarth,
          isActive: false,
        },
        {
          icon: IconLocation,
          isActive: true,
        }
      ],

      switchText: [
        {
          text: 'By Service',
          isActive: false,
        },
        {
          text: 'By Partner',
          isActive: true,
        }
      ]

    }
  },

  methods: {
    iconClick: function (index) {
      this.navMenu[this.activeNav].isActive = false;
      this.activeNav = index;
      this.navMenu[this.activeNav].isActive = true;

      console.log(this.navMenu)
    },


  },

}
</script>

<style>
*,
*::before,
*::after {
  box-sizing: border-box;
}

/* Убираем внутренние отступы */
ul[class],
ol[class] {
  padding: 0;
}

/* Убираем внешние отступы */
body,
h1,
h2,
h3,
h4,
p,
ul[class],
ol[class],
li,
figure,
figcaption,
blockquote,
dl,
dd {
  margin: 0;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2D2D2D;
}

.container {
  display: flex;
}

.nav-menu {
  display: flex;
  flex-direction: column;
  height: 100vh;
  background-color: #2D2D2D;
}

.nav-menu_text {
  display: flex;
  align-items: flex-end;
  justify-content: center;

  flex-grow: 1;
  color: #FBBC05;
  padding-bottom: 20px;
}

.header-container{
  width: 100%;
}

.header{
  display: flex;
  justify-content: space-between;
  padding: 17px;
}

.header__center{
  margin: 0 20px;
  background-color: #F8F8FA;
  border-radius: 12px;
  overflow: hidden;
  flex-grow: 1;
}

.search-container{
  display: flex;
  padding: 0 17px 17px 17px;
}

.search__input{
  flex-grow: 1;
}

.search-setting{
  display: flex;
}

.search-setting__slider{
  display: flex;
  align-items: center;
  padding: 12px;
  background-color: #F8F8FA;
  border-radius: 12px;
}
</style>
