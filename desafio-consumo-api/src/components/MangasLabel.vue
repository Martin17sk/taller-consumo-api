<template>
    <div>
        <h1>Mangas API</h1>
        <p>{{ info }}</p>
        <button @click="getInfo()">Solicitar informacion</button>
    </div>
</template>

<script setup>
import { ref } from 'vue'
import axios from 'axios'

let info = ref('')

const getInfo = async () => {
  await axios.get('https://api.jikan.moe/v4/random/manga')
    .then(response => {
      info.value = response.data
    })
}
</script>

<style scoped>
    p {
        width: 300px;
    }
</style>