<script setup>
import { ref } from "vue";

const valor2 = ref("");
const valor1 = ref("");
</script>
<template>
<div>
  <input type="number" v-model="valor1" placeholder="Valor da conta" />

  <select name="Qualidade de serviço" id="asd" v-model="gorgeta">
    <option value="5">5%(Pessimo)</option>
    <option value="10">10%(Ruim)</option>
    <option value="15">15%( Mais ou menos)</option>
    <option value="20">20%(Bom)</option>
    <option value="25">25%(Perfeito)</option>
  </select>

  <input type="number" placeholder="quantidade de amigos" v-model="valor2" />

  <p>Valor para cada um pagar: {{ (valor1 * (1 + gorgeta / 100)) / valor2 }}</p>
</div>
</template>
