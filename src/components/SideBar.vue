<template>
  <div class="Sidebar">
    <!-- <b-button v-b-toggle.sidebar-no-header>Toggle Sidebar</b-button> -->
    <b-sidebar
      bg-variant="light"
      id="sidebar-no-header"
      aria-labelledby="sidebar-no-header-title"
      no-header
      shadow
      visible
    >
      <img src="../assets/logo.png" class="pic" alt="" />
      <div class="bg-light text-dark menu" v-for="n in menu" :key="n">
        <strong class="mr-auto">{{n}}</strong>
      </div>
    </b-sidebar>
  </div>
</template>

<script>
export default {
  data(){
    return{
      menu:["Home","About","Vue","Map","User"]
    }
  }


};
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Kanit&display=swap');

.SideBar {
  grid-area: SideBar;
  border: 10px;
  border-color: black;
  margin: 60px 50% 20px 20px;
}
#sidebar-no-header {
  width: 19%;
}
@media screen and (max-width: 600px) {
  #sidebar-no-header {
    visibility: hidden;
    clear: both;
    float: left;
    margin: 10px auto 5px 20px;
    width: 28%;
    display: none;
  }
}
.menu{
  padding: 15px;
  text-align: center;
}
.pic{
  display: block;
  margin-left: auto;
  margin-right: auto;
  width: 50%;
  margin-top: 20px;
  margin-bottom: 50px;
}
</style>
