<script setup>
import { ref } from 'vue'

const msg = ref('Compute Product')
const num1 = ref(0)
const num2 = ref(0)
const result = ref(null)

function Total() {
  result.value = num1.value * num2.value}

</script>

<template>
  <div class="container">
  <h1>{{ msg }}</h1>
  <div class="input-group">
  <input type="number" v-model.number="num1" placeholder="Enter first number" />
    <input type="number" v-model.number="num2" placeholder="Enter second number" />
    </div>
    <button v-if="result === null" @click="Total">Compute</button>
    <p v-if="result !== null">Result: {{ result }}</p>
</div>
  </template>


<style>
body{
  background-image: url(https://g.foolcdn.com/editorial/images/539523/airplane-takeoff-getty.jpg);
  background-repeat: no-repeat;
  background:cover;
  background-size: cover;
}
.container {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  height: 100vh;
  gap: 20px; 
}
.input-group {
  display: flex;
  gap: 10px;
}
</style>