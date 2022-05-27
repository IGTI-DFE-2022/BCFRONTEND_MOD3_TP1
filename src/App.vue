<script setup>
import Conversor from "./components/Conversor.vue";
</script>

<template>
  <div class="container">
    <div class="header">Reais Para Dolares</div>
    <Conversor></Conversor>
  </div>
</template>

<style>
@import "assets/base.css";

.container {
  display: flex;
  flex-flow: column nowrap;
  align-items: center;
}

.header {
  line-height: 1.5;
  font-size: 2rem;
  font-weight: bold;
  margin-bottom: 1rem;
}
</style>
