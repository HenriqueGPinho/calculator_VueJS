<script setup>
  import { reactive } from 'vue';

  const state = reactive({
    firstValue: 0,
    secondValue: 0,
    operator: 'addition',
    result: 0
  })

</script>

<template>
  <div class="container">
    <header class="p-4 mt-3 mb-3 text-center bg-light rounded-3">
      <h1>Calculadora VueJS</h1>
    </header>
    <form class="row justify-content-evenly">
      <input @keyup="e => state.firstValue = e.target.value" type="number" placeholder="valor 1" class="m-1 col-3">
      <select class="m-1 col-3">
        <option value="addition">+</option>
        <option value="subtraction">-</option>
        <option value="multiplication">x</option>
        <option value="division">:</option>
      </select>
      <input type="number" placeholder="valor 2" class="m-1 col-3">
    </form>
    <h2 class="p-3 mt-3 mb-3 text-center bg-light rounded-3">{{ state.firstValue }}</h2>
  </div>
</template>

<style scoped>

</style>
