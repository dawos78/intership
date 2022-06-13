<template>
  <div class="SideBar">
    <nav class="mb-3">
      <b-nav vertical>
        <img src="../assets/logo.png" style="margin: 20px" alt="" />
        <b-nav-item active>หน้าหลัก</b-nav-item>
        <b-nav-item active>เกี่ยวกับ</b-nav-item>
        <b-nav-item active>แผนที่</b-nav-item>
        <b-nav-item active>ไปนู้น</b-nav-item>
        <b-nav-item active>ไปนี่</b-nav-item>
      </b-nav>
    </nav>
  </div>
</template>

<script>
export default {};
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Kanit&display=swap');

.SideBar {
  grid-area: SideBar;
  border: 10px;
  border-color: black;
}
.nav-item.nav-item.nav-item a {
  font-family: 'Kanit', sans-serif;
  color: red;
  text-align: center;
  text-underline-position: none;
  font-weight: bold;
}
</style>
