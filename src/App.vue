<template>
  <div class="container">
    <DropDown v-if="dropDown.show"/>

    <div class="navbg" id="navbg1">&nbsp;</div>
    <div class="navbg" id="navbg2">&nbsp;</div>

    <nav class="topbar">
      <div id="nav1">test</div>
      <div id="nav2">
        <HamburgerSelect height="2em" width="2em" color="#F6C900" :drop="dropDown.show" @click="handleClick"/>
      </div>
      <div id="nav3">
        test
      </div>
    </nav>
  </div>


  <router-view/>
</template>

<script setup lang="ts">
  import HamburgerSelect from './components/HamburgerSelect.vue'
  import DropDown from './components/DropDown.vue'
  import { reactive } from 'vue'

  const dropDown = reactive({ show: false })

  const handleClick = () => {
    dropDown.show = !dropDown.show
    console.log(dropDown.show)
  }
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Nunito:ital,wght@0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;0,1000;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900;1,1000&display=swap');

:root {
  --main-text: #80FF72;

  --main-bg: #171123;
  --light-bg: #F4F8F6;
}

* {
  margin: 0;
  padding: 0;

}

#app {
  font-family: 'Nunito', sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
}

body {
  background-color: var(--main-bg);
}

@media screen and (max-width: 450px) {
  nav.topbar {
    display: flex;
    height: 5em;
    width: 100%;
    align-items: center;
  }

  nav.topbar>div {
    flex: 1;
    font-size: 2rem;
  }

  nav.topbar>div#nav2 {
    transform: translateY(20px) rotate(90deg);

  }

  .container {
    overflow-x: hidden;
    position: relative;
    width: 100%;
    height: 15vh;
  }

  div.navbg {
    position: absolute;
    background-color: var(--light-bg);
    z-index: -5;
    overflow-x: visible;
  }

  div#navbg1 {
    left: 24%;
    transform: rotate(-8deg) scaleX(65) scaleY(6);
  }
  
  div#navbg2 {
    left: 75%;
    transform: rotate(8deg) scaleX(65) scaleY(6);
  }
  


}


@media screen and (min-width: 450px) {
  nav.topbar {
    display: flex;
    height: 5em;
    width: 100%;
  }
  
  nav.topbar>div {
    flex: 1;
  
  }
  
  nav.topbar>div#nav1 {
    background-color: aqua;
  }
  
  nav.topbar>div#nav2 {
    background-color: aqua;
  }

}

</style>
