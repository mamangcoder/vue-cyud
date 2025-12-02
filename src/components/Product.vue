<script setup>
import { ref, watch, watchEffect } from 'vue'

const productId = ref('')
const product = ref(null)

watch(productId, async (newValue, oldValue) => {
  if (newValue) {
    const response = await fetch(`/${newValue}.json`)
    product.value = await response.json()
  } else {
    product.value = null
  }
})
</script>

<template>
  <label for="productId">
    Product Id :
    <select name="" id="" v-model="productId">
      <option value="product1">Product 1</option>
      <option value="product2">Product 2</option>
      <option value="product3">Product 3</option>
      <option value="product4">Product 4</option>
    </select>
  </label>

  <div v-if="product">
    <h1>Product</h1>
    <p>Id : {{ product.id }}</p>
    <p>name : {{ product.name }}</p>
    <p>Price : {{ product.price }}</p>
  </div>
</template>

<style></style>
