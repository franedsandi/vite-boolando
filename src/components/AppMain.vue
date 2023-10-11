<script>
import Menus from '../data/Menus';

export default {
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
        <div v-for="(item, index) in cards" :key="index" class="card">
          <div class="image">
            <img :src="item.primaryImage" alt="articulo">
            <img :src="item.secondaryImage" alt="articulo b" class="upper p-absolute">
            <div class="like p-absolute">
              <span class="heart" >&hearts;</span>
            </div>
            <div class="caracteristicas p-absolute">
              <span v-if="item.discount !== null" class="sconto">{{ item.discount }}</span>
              <span class="sostenibile" v-if="item.sostenibilita">Sostenibilità</span>
            </div>
          </div>
            <div class="description">
              <span class="tag brand">{{ item.marca }}</span>
              <span class="tag name">{{ item.modello }}</span>
              <span class="tag price">
              <span v-if="item.lastPrice !== null" class="red">{{ item.lastPrice }} &euro;</span>
              <span class="fullprice">{{item.fullPrice}}&euro;</span>
            </span>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
@use '../scss/partials/mid.scss';

</style>