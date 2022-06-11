<template>
  <div class="home">
    <div>
      <!-- zone input -->
      <b-card style="max-width: auto" class="m-5">
        <b-container class="bv-example-row">
          <b-row class="justify-content-md-center">
            <b-col col lg="5">
              <h1 style="text-align: center;">Calculator vue</h1>
              <br />
              <label for="input-none">Input 1 :</label><br />
              <b-input-group>
                <b-form-input
                  id="input1"
                  type="number"
                  min="0"
                  v-model="input1"
                  :disabled="
                    selected === '+' ||
                    selected === '-' ||
                    selected === '*' ||
                    selected === '÷'
                  "
                  autofocus
                ></b-form-input>
                <b-input-group-append>
                  <b-button variant="outline-primary" @click="deletevalue1()"
                    >Delete</b-button
                  >
                </b-input-group-append>
              </b-input-group>

              <label for="input-none">Input 2 :</label><br />
              <b-input-group>
                <b-form-input
                  id="input2"
                  type="number"
                  min="0"
                  v-model="input2"
                ></b-form-input>
                <b-input-group-append>
                  <b-button variant="outline-primary" @click="deletevalue2()"
                    >Delete</b-button
                  >
                </b-input-group-append>
              </b-input-group>

              <!-- oparator -->
              <br /><b-form-select
                v-model="selected"
                :options="options"
                @change="select()"
              ></b-form-select>
              <!-- oparator -->

              <br /><br /><strong
                ><label
                  >Result : {{ input1 }} {{ selected }} {{ input2 }} = {{ sum }}
                </label></strong
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
            >{{ number }}</b-button
          >
        </div>
        <div class="btopa">
          <b-button variant="outline-dark" @click="sumresult()">Sum</b-button>
          <b-button variant="outline-dark m-2" @click="resetvalue()"
            >Clear</b-button
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
      input1: '',
      input2: '',
      logtest: false,
      selected: null,
      options: [
        { value: null, text: 'ไม่เลือก' },
        { value: '+', text: 'บวก' },
        { value: '-', text: 'ลบ' },
        { value: '*', text: 'คูณ' },
        { value: '÷', text: 'หาร' },
      ],
      sum: 0,
    };
  },
  methods: {
    setnum(index) {
      if (index === 0 && this.input1 === '') {
        alert('ใส่ 0 ก่อนไม่ได้นะค้าบ');
      } else if (index === 0 && this.input2 === '') {
        alert('ใส่ 0 ก่อนไม่ได้นะค้าบ');
      } else {
        if (this.logtest == true) {
          this.input2 += index;
        } else {
          this.input1 += index;
        }
      }
    },
    select() {
      if (this.input1 == '') {
        alert('กรุณาใส่ข้อมูลช่องแรกก่อนครับ');
        this.input1 = '';
        this.input2 = '';
        this.selected = null;
        this.sum = 0;
        this.logtest = false;
      } else {
        this.logtest = true;
      }
    },
    sumresult() {
      if (this.selected === '+') {
        this.sum = parseFloat(this.input1) + parseFloat(this.input2);
        console.log(this.input1);
        console.log(this.input2);
        console.log(this.sum);
        alert('เลือกบวก');
      } else if (this.selected === '-') {
        alert('เลือกลบ');
        this.sum = parseFloat(this.input1) - parseFloat(this.input2);
      } else if (this.selected === '*') {
        alert('เลือกคุณ อิอิ');
        this.sum = parseFloat(this.input1) * parseFloat(this.input2);
      } else if (this.selected === '÷') {
        alert('เลือกลบหาร');
        this.sum = parseFloat(this.input1) / parseFloat(this.input2);
      }
    },
    resetvalue() {
      this.input1 = '';
      this.input2 = '';
      this.selected = null;
      this.sum = 0;
      this.logtest = false;
    },
    deletevalue1() {
      this.input1 = this.input1.toString().slice(0, -1);
    },
    deletevalue2() {
      this.input2 = this.input2.toString().slice(0, -1);
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
