<template>
  <div>
    <b-card no-body class="text-center">
      <div class="bg-white text-dark" style="width: 100%; height: 100%">
        <div style="width: 20%; margin: auto">
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
          <Br></Br>
          <div class="mt-2">Value: {{ sumvalue }}</div>
        </div>
      </div>
    </b-card>
  </div>
</template>

<script>
export default {
  data() {
    return {
      input1:'12',
      input2:'3',
    };
  },
  computed: {
    sumvalue() {
      return this.sum = parseFloat(this.input1) + parseFloat(this.input2);
    },
  },
};
</script>

<style></style>
