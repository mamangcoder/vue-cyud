<script setup>
let count = 0

function increment() {
  console.info(`Increment counter : ${count}`)
  count++
}
</script>

<template>
  <div>
    <h1>Counter : {{ count }}</h1>
    <button v-on:click="increment"></button>
  </div>
</template>

<style scoped></style>
