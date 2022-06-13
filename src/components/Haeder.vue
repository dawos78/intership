<template>
    <div class="haederSection">
    <b-list-group class="justify-content-center ">
    <b-list-group-item>
      <b-avatar button @click="onClick" variant="primary" text="G" class="align-baseline"></b-avatar>
      Got'Ji
    </b-list-group-item>
  </b-list-group>
    </div>
</template>

<script>
  export default {
    methods: {
      onClick() {
        this.$bvModal.msgBoxOk('Username: ggthkk.\n Email: babagatom@gmail.com', {
          title: 'รายละเอียด',
          size: 'md',
          buttonSize: 'md',
          okVariant: 'success',
          headerClass: 'p-2 border-bottom-0',
          footerClass: 'p-2 border-top-0'
        })
      }
    }
  }
</script>

<style>
.haederSection{
    grid-area: haederSection;
    margin-top: 10px;
    text-align: right;
}
</style>