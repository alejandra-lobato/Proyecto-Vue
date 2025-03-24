<template>
  <div>
    <h2>Lista De Tareas</h2>
    <input type="text" v-model="nuevaTarea" @keyup.enter="addTarea"> <!---->
    <ul>
      <li v-for="(tarea, index) in tareas" :key="index"> <!-- v-for es una directiva para representar una lista de elementos basados en en a matriz -->
        {{ tarea }}
        <button @click="borrarTarea">Borrar</button>               <!-- :key esta directiva nos permite identificar cada elemento de una lista de forma unica -->
      </li>
    </ul>
  </div>
</template>

<script setup>
import {ref} from 'vue';
const tareas = ref ([]);
const nuevaTarea = ref ('');

const addTarea = () =>{
  tareas.value.push(nuevaTarea.value); // metodo puch coloca al final de la fila el elemento ingresado
  nuevaTarea.value = '';
}

const borrarTarea = (index) => {
  tareas.value.splice(index,1);
}
</script>

<style>
</style>