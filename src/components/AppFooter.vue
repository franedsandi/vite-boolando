<script>
export default {
  data(){
    return{
      legal:[
        {
          href: '#',
          text: 'Informazioni legali'
        },
        {
          href: '#',
          text: 'Informativa sulla Privacy'
        },
        {
          href: '#',
          text: 'Dirito di recesso'
        }
      ],
      social:[
        {
          href: '#',
          icon: '<i class="fa-brands fa-square-twitter"></i>'
        },
        {
          href: '#',
          icon: '<i class="fa-brands fa-square-facebook"></i>'
        },
        {
          href: '#',
          icon: '<i class="fa-brands fa-square-instagram"></i></i>'
        },
        {
          href: '#',
          icon: '<i class="fa-brands fa-pinterest"></i>'
        },
        {
          href: '#',
          icon: '<i class="fa-brands fa-youtube"></i>'
        },
      ]
    }
  }
}
</script>

<template>
  <div class="footer">
    <div class="container d-flex f-wrap s-between">
      <div class="legal">
        <span class="compani">
          Boleando S.R.L.
        </span>
        <ul class="d-flex f-wrap s-between">
          <li 
          v-for="(item,index) in legal"
          :key="index">
            <a 
            :href="item.href">
            {{item.text}}</a>
          </li>
        </ul>
      </div>
      <div class="social">
        <span>
          Trovaci anche su
        </span>
        <ul class="d-flex f-wrap s-between">
          <li 
          v-for="(item, index) in social"
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
@use '../scss/partials/_footer.scss';

</style>