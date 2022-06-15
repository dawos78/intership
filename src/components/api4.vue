<template>
  <div>
    <b-card no-body class="text-center">
      <div
        class="bg-white text-dark"
        style="width: 40%; margin: auto; height: 100%"
      >
        input1
        <b-form-input
          v-model="input1"
          placeholder="Enter your input 1"
        ></b-form-input
        ><br />
        <p>+</p>
        input2
        <b-form-input
          v-model="input2"
          placeholder="Enter your input 2"
        ></b-form-input
        ><br />
        <b-button block variant="info" @click="sumvalue">sum</b-button><Br></Br>
        <div class="mt-2">Value: {{ sum }}</div>
      </div>
    </b-card>
  </div>
</template>

<script>
export default {
  data() {
    return {
      input1: 0,
      input2: 0,
      sum: '',
    };
  },
  methods: {
    sumvalue() {
      this.sum = parseFloat(this.input1) + parseFloat(this.input2);
    },
  },
};
</script>

<style></style>
