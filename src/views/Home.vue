<template>
  <div class="home">
    <div>
      <!-- zone input -->
      <b-card style="max-width: auto" class="m-5">
        <b-container class="bv-example-row">
          <b-row class="justify-content-md-center">
            <b-col col lg="5">
              <label for="input-none">Input 1 :</label>
              <b-form-input
                id="input1"
                v-model="input1" 
                :disabled="
                  selected === '+' ||
                  selected === '-' ||
                  selected === '*' ||
                  selected === '÷'
                "
              ></b-form-input>
              <label for="input-none">Input 2 :</label><br />
              <b-form-input id="input2" v-model="input2"></b-form-input>

              <!-- oparator -->
              <br /><b-form-select
                v-model="selected"
                :options="options"
                @change="select()"
              ></b-form-select>
              <!-- oparator -->

              <br /><br /><strong
                ><label>Result : {{ input1 }} {{ selected }} {{ input2 }} = </label></strong
              >
            </b-col>
          </b-row>
        </b-container>
        <!-- zone input -->

        <div class="bt">
          <b-button
            v-for="(number, index) in number"
            :key="index"
            variant="outline-primary m-1"
            @click="setnum(index)"
            >{{ number }}</b-button>
        </div>
        <div class="btopa">
          <b-button variant="outline-dark" @click="resetInput">Clear</b-button>
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
      input1: '',
      input2: '',
      logtest:false,
      selected: null,
      options: [
        { value: null, text: 'ไม่เลือก' },
        { value: '+', text: 'บวก' },
        { value: '-', text: 'ลบ' },
        { value: '*', text: 'คูณ' },
        { value: '÷', text: 'หาร' },
      ],
    };
  },
  methods: {
    setnum(index) {

      if(this.logtest == true){
        this.input2 += index;
        
      }else{
        this.input1 += index;
      }
      console.log(this.logtest)
        
    },
    select(){
      this.logtest = true
    },
    resetInput() {
      this.input1 = "";
      this.input2 = "";
      this.logtest = flase;
      this.selected.options.value == null
    },
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

.btopa {
  display: block;
  text-align: center;
  border: none;
  margin-top: 30px;
  border-radius: 6px;
}
</style>
