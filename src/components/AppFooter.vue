<script>
import social from '../data/social';
import legal from '../data/legal';
export default {
  data(){
    return{
      legal,
      social,
    }
  }
}
</script>

<template>
  <div class="footer">
    <div class="container">
      <div class="legal">
        <span class="compani">
          Boleando S.R.L.
        </span>
        <ul>
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
        <ul>
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