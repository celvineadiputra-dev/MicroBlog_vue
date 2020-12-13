<template>
  <BaseNavbar/>
  <router-view/>
</template>

<script>
import BaseNavbar from '@/components/BaseNavbar/BaseNavbar.vue';
export default {
  components:{
    BaseNavbar,
  },
};
</script>

<style lang="scss">
@import "./assets/scss/style.scss";
</style>
