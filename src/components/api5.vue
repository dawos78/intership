<template>
  <div>
    <b-card no-body class="text-center">
      <div class="bg-white text-dark" style="width: 100%; height: 100%">
      <br><br>
      <div
        class="bg-white text-dark"
        style="width: 40%; margin: auto; height: 100%"
      ><p>ใส่น้ำหนักตัวเอง</p>
        <b-form-input v-model="w" placeholder="ใส่น้ำหนักตัวเอง"></b-form-input>
        <div class="mt-2">Value: {{ w }}</div>
      </div>
      <br><br>
      </div>
    </b-card>
  </div>
</template>

<script>
export default {
  data() {
    return{
      w: 0,
    }

  },
  watch: {
    w(value) {
      if(value >= 200){
        setTimeout(() => {
          alert("น้ำหนักเยอะเกินไปนะค้าบ ไม่ใช่คนปกติละ")
          this.w = 0
        }, 1000);
      }
    }
  },
};
</script>

<style></style>
