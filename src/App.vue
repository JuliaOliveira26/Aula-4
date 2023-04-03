<script setup>
import { ref } from "vue";
const name = ref(``)
const idade = ref();
const email = ref(``)
let mostrardiv = ref(true)
const nome2 = ref('')
const idadeF2 = ref()
const emailF2 = ref('')

</script>

<template>
  <h1> Formulários</h1>
  <br>
  <div>
    <label>Nome:</label>
    <input type="text" v-model="name" />

  
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
    <input type="text" v-model="email" />
  </div>


  <div class="Enviar">
    <button @click="mostrardiv= !mostrardiv"> Enviar </button>
    <div v-if = "mostrardiv">
    <p>Nome:{{ name }}</p>
    <p>Idade:{{ idade }}</p>
      <p>E-mail:{{ email }}</p>
</div>
  </div>
 <form @submit.prevent='formulario1'>
  <h1>Formulário 2 </h1>
  <br>
  <div>
    <label>Nome:</label>
    <input type="text" v-model="nome2" minlength="3" maxlength="20" />

  
    <button @click="nome2= ``">Limpar</button>
  </div>
  <br>
  <div>
    <label>idade:</label>
    <input type="number" v-model="idadeF2"  date id="datemax" name="datemax" max="60" />
    <input type="date" id="datemin" name="datemin" min="18">"
    <button @click="idadeF2 = ``">Limpar</button>
  </div>
  <br>
  <div>
    <label> E-mail:</label>
    <input type="text" v-model="emailF2" />
  </div>


  <div class="Enviar">
    <button @click="mostrardiv= !mostrardiv"> Enviar </button>
    <div v-if = "mostrardiv">
      <p>Os dados enviados foram:</p>
    <p>Nome:{{ nome2 }}</p>
    <p>Idade:{{ idadeF2 }}</p>
      <p>E-mail:{{ emailF2}}</p>
</div>
  </div>



</form>


<br>




</template>

<style>
h1{
  text-align: center;
  font-size: 20px;
  
}
</style>