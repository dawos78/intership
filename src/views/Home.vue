<template>
  <div class="home">
    <SideBar></SideBar>
    <Haederpage></Haederpage>
    <Main></Main>
    <Footer></Footer>
  </div>
</template>

<script>

import Main from '../components/Main.vue'
import Haederpage from '../components/Haeder.vue'
import SideBar from '../components/SideBar'
import Footer from '../components/Footer.vue'

export default {
  components: {
    SideBar,
    Main,
    Haederpage,
    Footer,
  },
};
</script>

<style>
.home{
  
  display: grid;
  box-sizing: border-box;
  grid-template-rows: 1fr 6fr 1fr;
  grid-template-columns: 1fr 3fr 1fr;
  gap: 2px;
  height: 100vh;

  grid-template-areas: 
  "SideBar haederSection haederSection"
  "SideBar mainsection mainsection"
  "SideBar FooterSection FooterSection"
}
</style>
