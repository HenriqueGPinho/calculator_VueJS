<script setup>
  import { reactive } from 'vue';

  const state = reactive({
    firstValue: '',
    secondValue: '',
    operator: 'division',
    result: ''
  })

  const calculate = () => {
    const { operator } = state;

    switch (operator) {
      case 'subtraction':
        return state.result = state.firstValue - state.secondValue;
      case 'multiplication':
        return state.result = state.firstValue * state.secondValue;
      case 'division':
        return state.result = state.firstValue / state.secondValue;
      default:
        console.log(operator)
        return state.result = state.firstValue + state.secondValue;
    }
  }

</script>

<template>
  <div class="container">
    <header class="p-4 mt-3 mb-3 text-center bg-light rounded-3">
      <h1>Calculadora VueJS</h1>
    </header>
    <form class="row justify-content-evenly">
      <input @keyup="e => {state.firstValue = parseFloat(e.target.value); calculate()}" type="number" placeholder="valor 1" class="m-1 col-3">
      <select @change="e => {state.operator = e.target.value; calculate()}" class="m-1 col-3">
        <option value="addition">+</option>
        <option value="subtraction">-</option>
        <option value="multiplication">x</option>
        <option value="division">:</option>
      </select>
      <input @keyup="e => {state.secondValue = parseFloat(e.target.value); calculate()}" type="number" placeholder="valor 2" class="m-1 col-3">
    </form>
    <h2 class="p-3 mt-3 mb-3 text-center bg-light rounded-3">{{ state.result }}</h2>
  </div>
</template>

<style scoped>

</style>
