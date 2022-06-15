<template>
  <div class="FooterSection">
    <b-container class="bv-example-row">
      <b-row id="hidemenu">
        <b-col cols="2" v-for="(n, index) in btShowdata" :key="index"
          ><div>
            <b-card no-body class="text-center">
              <div class="bg-light text-dark" style="width: 100%; height: 100%">
                <b-button block variant="info" @click="goToEvents(index)">{{
                  n
                }}</b-button>
              </div>
            </b-card>
          </div></b-col
        >
      </b-row>
    </b-container>
  </div>
</template>

<script>
import api1 from '../components/api1.vue';
import api2 from '../components/api2.vue';
import api3 from '../components/api3.vue';
import api4 from '../components/api4.vue';
import api5 from '../components/api5.vue';
import api6 from '../components/api6.vue';
export default {
  components: {
    api1,
    api2,
    api3,
    api4,
    api5,
    api6,
  },
  data() {
    return {
      btShowdata: [
        'Api Data',
        'Api Componant',
        'Api Computed',
        'Api Methods',
        'Api watch',
        'Api Props',
      ],
    };
  },
  methods: {
    goToEvents(index) {
      if (index === 0) {
        location.href = 'https://vuejs.org/api/options-state.html#data';
      } else if (index === 1) {
        location.href = 'https://vuejs.org/guide/essentials/component-basics.html';
      }else if (index === 2) {
        location.href = 'https://vuejs.org/api/options-state.html#computed';
      }else if (index === 3) {
        location.href = 'https://vuejs.org/api/options-state.html#methods';
      }else if (index === 4) {
        location.href = 'https://vuejs.org/api/options-state.html#watch';
      }else if (index === 5) {
        location.href = 'https://vuejs.org/api/options-state.html#props';
      }
    },
  },
};
</script>

<style>
.FooterSection {
  grid-area: FooterSection;
}
@media screen and (max-width: 600px) {
  #hidemenu {
    visibility: hidden;
    clear: both;
    float: left;
    margin: 10px auto 5px 20px;
    width: 28%;
    display: none;
  }
}
</style>
