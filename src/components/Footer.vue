<template>
    <div class="FooterSection">
        <api1></api1>
    </div>
</template>

<script>
import api1 from '../components/api1.vue'
export default{
    components:{
        api1,
    }
}
</script>

<style >
.FooterSection{
    grid-area: FooterSection;
}
</style>
