<script>
export default {
  data(){
    return{
      mainMenu:[
        {
          href: '#',
          text: 'Donna'
        },
        {
          href: '#',
          text: 'Uomo'
        },
        {
          href: '#',
          text: 'Bambini'
        }
      ],
      secondMenu:[
        {
          href: '#',
          text: '<i class="fa-regular fa-user"></i>'
        },
        {
          href: '#',
          text: '<i class="fa-regular fa-heart"></i>'
        },
        {
          href: '#',
          text: '<i class="fa-solid fa-bag-shopping"></i>'
        }
      ]
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
      <img src="../assets/img/boolean-logo.png" alt="">
    </div>
    <div class="fontawesome">
      <ul>
        <li 
          v-for="(item, index) in secondMenu"
          :key="index">
            <a 
            :href="item.href" 
            v-html="item.text"></a>
        </li>
      </ul>
    </div>
  </div>

</div>
</template>

<style lang="scss" scoped>
@use '../scss/partials/header.scss';

</style>