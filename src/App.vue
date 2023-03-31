<script setup>
import { ref } from "vue";
const name = ref(``)
const idade = ref();

</script>

<template>
  <h1> Formulários</h1>
  <br>
  <div>
    <label>Nome:</label>
    <input type="text" v-model="name" />

    <p>Nome: {{ name }}</p>
    <button @click="name = ``">Limpar</button>
  </div>
  <br>
  <div>
    <label>idade:</label>
    <input type="number" v-model="idade" />
    <button @click="idade = ``">Limpar</button>
  </div>
  <br>
  <div>
    <label> E-mail:</label>
    <input type="text">
  </div>

<br>




</template>

<style>
h1{
  text-align: center;
  font-size: 20px;
  
}
</style>