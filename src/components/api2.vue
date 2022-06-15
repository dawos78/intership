<template>
  <div>
    <b-card no-body class="text-center">
      <div class="bg-white text-dark" style="width: 100%; height: 100%">
      <api1></api1>
      <api5></api5>
      </div>
    </b-card>
  </div>
</template>

<script>
import api1 from '../components/api1.vue';
import api5 from '../components/api5.vue';

export default {
  components: {
    api1,
    api5,
  },
};
</script>

<style></style>
