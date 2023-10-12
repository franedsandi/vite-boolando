<script>
import products from '../data/products';
import productCard from './ProductCard.vue'; 

export default {
  components: {
    productCard, 
  },
  data() {
    return {
      cards: products.cards,
    };
  }
}
</script>

<template>
  <div class="mid">
    <div class="container">
      <div class="content">
        <productCard
          v-for="(product, index) in cards"
          :key="index"
          :productObj="product"
        />
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
@use '../scss/partials/mid.scss';
</style>