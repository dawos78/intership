<template>
  <div>
    <b-card no-body class="text-center">
      <div class="bg-white text-dark" style="width: 100%; height: 100%">
      <br><br>
        <div style="width: 20%; margin: auto">
          input :<b-form-input
            v-model="name"
            placeholder="Enter your name"
          ></b-form-input>
          <div class="mt-2">Value: {{ name }}</div>
        </div>
      </div>
      <br><br>
    </b-card>
  </div>
</template>

<script>
export default {
  data() {
    return {
      name: '',
    };
  },
};
</script>

<style></style>
