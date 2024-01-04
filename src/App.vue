<template>
    <div>
      <CardComponent 
      image="https://img.freepik.com/fotos-premium/anime-menino-homem-avatar-ai-arte-generativa_225753-7457.jpg"
      name="Lucas Dias"
      email="lucas.allx@hotmail.com"
      />
    </div>
</template>

<script setup>
import 'bootstrap/dist/css/bootstrap.css'
import CardComponent from './components/CardComponent.vue';

import { ref, onMounted } from "vue"

let userData = ref("")

const handleUserApiRequest = async () => {
  const req = await fetch(`https://reqres.in/api/users/`)
  const json = await req.json()
  userData.value = json.data
}

onMounted(() => {
  console.log('O componente foi montado no DOM!');
  handleUserApiRequest()
})

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