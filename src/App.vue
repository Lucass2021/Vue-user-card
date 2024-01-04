<template>
    <div>
      <CardComponent/>
    </div>
</template>

<script setup>
import 'bootstrap/dist/css/bootstrap.css'
import CardComponent from './components/CardComponent.vue';

</script>

<style>
*{
  box-sizing: border-box !important;
  padding:0px;
  margin:0px;
}

body{
  background: #1a1a1a;
}
</style>


<!-- Data:
https://reqres.in/api/users/
// const data = [
//   { id: '1', image: 'https://img.freepik.com/fotos-premium/anime-menino-homem-avatar-ai-arte-generativa_225753-7457.jpg', name: 'Nome 1', email: 'email1@example.com' },
// ]; -->