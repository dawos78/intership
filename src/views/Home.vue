<template>
  <div class="home">
    <div>
      <!-- zone input -->
      <b-card style="max-width: auto" class="m-5">
        <b-container class="bv-example-row">
          <b-row class="justify-content-md-center">
            <b-col col lg="5">
              <label for="input-none">Input 1 :</label>
              <b-form-input v-model="inpunt1"></b-form-input>
              <label for="input-none">Input 2 :</label><br />
              <b-form-input v-model="inpunt1"></b-form-input>
              <br /><br /><label for="input-none">Result : {{p}}</label>
            </b-col>
          </b-row>
        </b-container>
        <!-- zone input -->

        <!-- oparator -->

        <div class="mt-3 bt">
          <b-button variant="outline-success m-2" @click="plus('+')">&nbsp;+&nbsp;</b-button>
          <b-button variant="outline-danger m-2">&nbsp;-&nbsp;</b-button>
          <b-button variant="outline-secondary m-2">&nbsp;*&nbsp;</b-button>
          <b-button variant="outline-info m-2">&nbsp;÷&nbsp;</b-button>
        </div>

        <!-- oparator -->

        <div class="bt">
          <b-button
            v-for="(number, index) in number"
            :key="index"
            variant="outline-primary m-1"
            @click="setnum(index)"
            >{{ number }}</b-button
          >
        </div>
      </b-card>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      number: ['0', '1', '2', '3', '4', '5', '6', '7', '8', '9'],
      inpunt1: '',
      inpunt2: '',

    };
  },
  methods: {
    setnum(index) {
      this.inpunt1 += index;
    },
    plus(){
      this.p = '+'
      console.log(p);
    }
  },
};
</script>

<style>
.bt {
  display: block;
  text-align: center;
  border: none;
  margin-top: 30px;
  border-radius: 6px;
}
</style>
