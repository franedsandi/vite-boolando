<script>
export default {
  name: 'productCard',
  props: {
    productObj: Object
  },
};
</script>

<template>
  <div class="card">
    <div class="image">
      <img 
      :src="productObj.primaryImage" 
      alt="articulo">
      <img 
      :src="productObj.secondaryImage" 
      alt="articulo b" class="upper">
      <div class="like">
        <span class="heart" >&hearts;</span>
      </div>
      <div class="caracteristicas">
        <span 
        v-if="productObj.discount !== null" 
        class="sconto">
        {{ productObj.discount }}
      </span>
        <span 
        class="sostenibile" 
        v-if="productObj.sostenibilita">
        Sostenibilità
      </span>
      </div>
    </div>
    <div class="description">
      <span class="tag brand">{{ productObj.marca }}</span>
      <span class="tag name">{{ productObj.modello }}</span>
      <span class="tag price">
        <span 
        v-if="productObj.lastPrice !== null" 
        class="red">
        {{ productObj.lastPrice }} &euro;
      </span>
        <span 
        class="fullprice">
        {{ productObj.fullPrice }}&euro;
      </span>
      </span>
    </div>
  </div>
</template>

<style lang="scss" scoped>
@use '../scss/partials/card.scss';
</style>