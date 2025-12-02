<script setup>
import { ref } from 'vue'

const titleClass = ref('title')
const gambar = [
  'https://picsum.photos/300/200?random=1',
  'https://picsum.photos/300/200?random=2',
  'https://picsum.photos/300/200?random=3'
]

const currentImage = ref(gambar[0])
let index = 0

function gantiGambar() {
  index = (index + 1) % gambar.length
  currentImage.value = gambar[index]
}
</script>

<template>
  <h1 v-bind:class="titleClass">Make me red</h1>
  <div>
    <img :src="currentImage" width="300">
    <br><br>
    <button @click="gantiGambar">Ganti Gambar</button>
  </div>
</template>

<style>
.title {
  color: red;
}
</style>
