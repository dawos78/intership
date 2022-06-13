<template>
  <div class="home">
    <div>
      <!-- zone input -->
      <b-card style="text-align: center" class="m-5">
        <b-container class="bv-example-row">
          <b-row class="justify-content-md-center">
            <b-col>
              <h1 style="text-align: center">Home Page</h1>
              <br />
              <!-- เลือกเมนู -->
              <div v-for="(bt,index) in butTon" :key="index">
                <div>
                  <b-col>
                  <b-button variant="outline-primary m-1" @click="check(index)">{{ bt }}</b-button>
                  </b-col>
                </div>
              </div>
              <!-- เลือกเมนู -->
            </b-col>
          </b-row>
        </b-container>
      </b-card>
      <div v-if="this.open === 1">
        <Calculator></Calculator>
      </div>
    </div>
  </div>
</template>

<script>
import Calculator from './calculator.vue';
export default {
  components: {
    Calculator,
  },
  data() {
    return {
      open: 0,
      butTon:['Calculator','BMI'],
    };
  },
  methods: {
    check(index) {
      if (index === 0) {
        this.open = 1;
      } else if (index === 1) {
        this.open = 2;
      }
    }
  },
};
</script>

<style lang="scss" scoped></style>
