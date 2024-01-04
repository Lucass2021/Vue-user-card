<template>
    <div>
        <div class="container">
            <div class="row justify-content-center">
                <div class="card">
                    <img :src="props.image" alt="">
                    <h1>{{ props.name }}</h1>
                    <h2><a :href="`mailto:${props.email}`">{{ props.email }}</a></h2>
                </div>
            </div>
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
.container .row{
    margin: 50px 0px;
}

.card{
    background: #fff;
    width: 300px;
    padding:20px;
    border-radius: 10px;
    margin: 30px;
}

.card img{
    max-width: 90%;
    display: flex;
    margin:0 auto;
    margin-bottom: 10px;
    border-radius: 20px;
    padding-top:10px;
}

.card h1{
    font-size: 20px;
    text-align: center;
    margin-bottom: 0px;
}

.card h2{
    font-size: 16px;
    text-align: center;
}

.card h2 a{
    text-decoration: none;
    color: #000;
    font-weight: 400;
}

</style>

<!-- container: {
    backgroundColor: "#fff",
    marginHorizontal: 30,
    padding: 30,
    borderRadius: 15,
    marginVertical: 20,
},
image: {
    width: "100%",
    height: 200,
    borderRadius: 15,
    marginBottom: 20
},
fullName: {
    fontWeight: "bold",
    fontSize: 20,
    textAlign: "center",
    marginBottom: 0
},
email: {
    fontSize: 16,
    textAlign: "center",
    marginBottom: 15
}, -->