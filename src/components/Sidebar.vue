<template>
<div class="sidebar">
  <h2>Barra Lateral</h2>
  <ul>
    <li><router-link to="/contador">CONTADOR</router-link></li>
    <li><router-link to="/lista-de-tareas">LISTA DE TAREAS</router-link></li>
    <li><router-link to="/registrar">REGISTRAR</router-link></li>
  </ul>

</div>
</template>

<script setup>
</script>

<style>
.sidebar{
  width: 200px;
  background-color: #f0f0f0;
  padding: 20px;
}
</style>