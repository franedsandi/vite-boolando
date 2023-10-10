<script>
import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';
import AppFooter from './components/AppFooter.vue';

export default {
  components:{
    'custom-header': AppHeader,
    'custom-main': AppMain,
    'custom-footer': AppFooter,
  }
}
</script>

<template>
  <custom-header/>
  <custom-main/>
  <custom-footer/>
</template>

<style lang="scss">
@use './scss/main.scss';
</style>