<script>
import Menus from '../data/Menus';
import Card from './Card.vue'; 

export default {
  components: {
    Card, 
  },
  data() {
    return {
      cards: Menus.cards,
    };
  }
}
</script>

<template>
  <div class="mid">
    <div class="container">
      <div class="content">
        <Card
          v-for="(item, index) in cards"
          :key="index"
          :primaryImage="item.primaryImage"
          :secondaryImage="item.secondaryImage"
          :discount="item.discount"
          :sostenibilita="item.sostenibilita"
          :marca="item.marca"
          :modello="item.modello"
          :lastPrice="item.lastPrice"
          :fullPrice="item.fullPrice"
        />
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
@use '../scss/partials/mid.scss';
</style>