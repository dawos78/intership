<template>
  <div>
    <b-card no-body class="text-center">
      <div class="bg-white text-dark" style="width: 100%; height: 100%"></div>
      <h1>{{name}}</h1>
      <h1>{{depart}}</h1>
    </b-card>
  </div>
</template>

<script>
export default {
  name:"api6",
  props:["name","depart"],
};
</script>

<style></style>
