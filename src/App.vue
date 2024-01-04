<template>
  <div class="container">
    <h1 class="mt-5">Our Users:</h1>
    <div class="card-container">
      <CardComponent 
      v-for="user in userData" :key="user.id"
      :image="user.avatar"
      :name="`${user.first_name} ${user.last_name}`"
      :email="user.email"
      />
    </div>
  </div>
</template>

<script setup>
import 'bootstrap/dist/css/bootstrap.css'
import CardComponent from './components/CardComponent.vue';

import { ref, onMounted } from "vue"

let userData = ref({})

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
  box-sizing: border-box;
  padding:0px;
  margin:0px;
}

body{
  background: #1a1a1a;
}

.container h1:first-child{
  color: #fff;
  text-align: center;
  font-size: 3.125rem;
}

.card-container{
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
  justify-content: center;
}
</style>