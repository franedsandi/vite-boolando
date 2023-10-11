<script>
import Menus from '../data/Menus';
export default {
  data(){
    return{
      mainMenu: Menus.mainMenu,
      secondMenu: Menus.secondMenu,
    }
  }
}
</script>

<template>
<div class="header">
  <div class="container">
    <ul>
      <li 
      v-for="(item,index) in mainMenu"
      :key="index">
        <a 
        :href="item.href">
        {{item.text}}</a>
      </li>
    </ul>
    <div class="logo">
      <img src="img/boolean-logo.png" alt="">
    </div>
    <div class="fontawesome">
      <ul>
        <li 
          v-for="(item, index) in secondMenu"
          :key="index">
            <a 
            :href="item.href" 
            v-html="item.icon"></a>
        </li>
      </ul>
    </div>
  </div>

</div>
</template>

<style lang="scss" scoped>
@use '../scss/partials/header.scss';

</style>