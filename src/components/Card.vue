<script>
export default {
  props: {
    primaryImage: String,
    secondaryImage: String,
    discount: String,
    sostenibilita: Boolean,
    marca: String,
    modello: String,
    lastPrice: Number,
    fullPrice: Number,
  },
};
</script>

<template>
  <div class="card">
    <div class="image">
      <img 
      :src="primaryImage" 
      alt="articulo">
      <img 
      :src="secondaryImage" 
      alt="articulo b" class="upper">
      <div class="like">
        <span class="heart" >&hearts;</span>
      </div>
      <div class="caracteristicas">
        <span 
        v-if="discount !== null" 
        class="sconto">
        {{ discount }}
      </span>
        <span 
        class="sostenibile" 
        v-if="sostenibilita">
        Sostenibilità
      </span>
      </div>
    </div>
    <div class="description">
      <span class="tag brand">{{ marca }}</span>
      <span class="tag name">{{ modello }}</span>
      <span class="tag price">
        <span 
        v-if="lastPrice !== null" 
        class="red">
        {{ lastPrice }} &euro;
      </span>
        <span 
        class="fullprice">
        {{ fullPrice }}&euro;
      </span>
      </span>
    </div>
  </div>
</template>

<style lang="scss" scoped>
@use '../scss/partials/card.scss';
</style>