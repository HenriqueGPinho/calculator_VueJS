<script setup>

</script>

<template>
  <div class="container">
    <header class="p-5 mt-3 mb-3 text-center bg-light rounded-3">
      <h1>Calculadora VueJS</h1>
    </header>
    <form class="row">
      <input type="number" name="number1" id="number1" placeholder="primeiro valor" class="col-5">
      <select class="col-2">
        <option value="addition">+</option>
        <option value="subtraction">-</option>
        <option value="multiplication">x</option>
        <option value="division">:</option>
      </select>
      <input type="number" name="number2" id="number2" placeholder="segundo valor" class="col-5">
    </form>
    <h2 class="p-3 mt-3 mb-3 text-center bg-light rounded-3">25</h2>
  </div>
</template>

<style scoped>

</style>
