<template>
  <h1>卡片</h1>
  <h2>總共 {{ totalGood }} 個讚</h2>
  <GoodCard v-for="(card, i) in cards" :key="i" :img="card.img" :text="card.text" v-model:good="card.good"></GoodCard>
</template>

<!-- <script>
import { reactive, computed } from 'vue'
import GoodCard from './components/GoodCard.vue'
export default {
  components: {
    GoodCard
  },
  setup() {
    const cards = reactive([
      { img: 'https://github.com/rogeraabbccdd.png', text: 'rogeraabbccdd', good: true },
      { img: 'https://github.com/vuejs.png', text: 'Vue.js', good: true },
      { img: 'https://github.com/vitejs.png', text: 'Vite.js', good: true }
    ])
    const totalGood = computed(() => {
      return cards.filter(card => card.good).length
    })
    return { cards, totalGood }
  }
}
</script> -->

<script setup>
import { reactive, computed } from 'vue'
import GoodCard from './components/GoodCard.vue'

const cards = reactive([
  { img: 'https://github.com/rogeraabbccdd.png', text: 'rogeraabbccdd', good: true },
  { img: 'https://github.com/vuejs.png', text: 'Vue.js', good: true },
  { img: 'https://github.com/vitejs.png', text: 'Vite.js', good: true }
])
const totalGood = computed(() => {
  return cards.filter(card => card.good).length
})
</script>

<style>
*{
  color: red;
}
</style>