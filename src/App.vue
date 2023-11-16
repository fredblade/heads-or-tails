<script setup>

import { reactive, computed } from 'vue'

const coin = reactive({
      value: 3

    });
function coinflip() {
  coin.value = Math.floor(Math.random() * 2);
  console.log(coin.value);
}

</script>

<template>
  <div>
    <div>
      <h1 class="title is-1">Heads or tails</h1>
      <br>
      <button class="button" @click="coinflip">Click me!</button>
      <br>
      <br>
      <img v-if="coin.value === 0" class="image is-128x128" src="/src/assets/tails.png">
      <img v-if="coin.value === 1" class="image is-128x128" src="/src/assets/heads.png">
      <img v-if="coin.value === 3" class="image" src="/src/assets/coin.jpg">
    </div>

  </div>
</template>

<style scoped>
</style>
