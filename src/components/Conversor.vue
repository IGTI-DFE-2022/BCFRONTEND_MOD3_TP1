<script setup>
import { reactive } from "vue";

const state = reactive({ exchangeFactor: 5, valueInput: 100 });

function calculate() {
  return Math.round((100 * state.valueInput) / state.exchangeFactor) / 100;
}
</script>

<template>
  <div class="container">
    <div class="input">
      <input
        type="number"
        placeholder="Valor em Reais"
        v-model="state.valueInput"
      />
    </div>
    <div class="input">
      <input
        type="number"
        placeholder="Fator de Conversão"
        v-model="state.exchangeFactor"
      />
    </div>

    <div class="result">US$ {{ calculate().toFixed(2) }}</div>
  </div>
</template>

<style scoped>
.container {
  text-align: center;
}

input {
  padding: 1rem;
  margin: 0 0 1rem;
  font-size: 1.5rem;
  text-align: center;
}

.result {
  font-size: 2rem;
}
</style>