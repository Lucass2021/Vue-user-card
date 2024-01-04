<template>
    <div>
        <div class="card">
            <img :src="props.image" alt="">
            <h1>{{ props.name }}</h1>
            <h2><a :href="`mailto:${props.email}`">{{ props.email }}</a></h2>
        </div>
    </div>
</template>

<script setup>
import { defineProps } from 'vue';

const props = defineProps({
    image: String,
    name: String,
    email: String,
})

</script>

<style scoped>

.card{
    background: #fff;
    width: 18.75rem;
    padding:1.25rem;
    border-radius: 1.25rem;
    margin: 1.875rem;
}

.card img{
    display: flex;
    margin:0 auto;
    margin-bottom: 0.625rem;
    border-radius: 1.25rem;
    padding-top:0.625rem;
}

.card h1{
    font-size: 1.25rem;
    text-align: center;
    margin-bottom: 0px;
}

.card h2{
    font-size: 1rem;
    text-align: center;
}

.card h2 a{
    text-decoration: none;
    color: #000;
    font-weight: 400;
}

</style>