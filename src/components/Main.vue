<template>
  <div class="mainsection">
    <hr />
    <div>
      <b-tabs
        active-nav-item-class="font-weight-bold text-uppercase text-danger"
        active-tab-class="font-weight-bold text-success"
        content-class="mt-3"
        justified
        v-model="tabIndex"
      >
        <b-tab title="Data" active>
            <p><api1></api1></p>
        </b-tab>
        <b-tab title="Components"><p><api2></api2></p></b-tab>
        <b-tab title="Computed"><p><api3></api3></p></b-tab>
        <b-tab title="Methods"><p><api4></api4></p></b-tab>
        <b-tab title="Watch"><p><api5></api5></p></b-tab>
        <b-tab title="Props"><p><api6 :name="testvalue" depart="Test"></api6></p></b-tab>
      </b-tabs>
    </div>
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
      testvalue: 'gotji'
    }
  },
}

</script>

<style>
.mainsection {
  grid-area: mainsection;
}
</style>
