<template>
    <div>
        <h1>Countries API</h1>
        <p>{{ info }}</p>
        <p v-for="(country, index) in countries" :key="index">{{ country.country }}</p>
        <button @click="getInfo()">Solicitar informacion</button>
    </div>
</template>

<script setup>
import { ref } from 'vue'
import axios from 'axios'

let info = ref('')
let countries = ref([])

const getInfo = async () => {
  await axios.get('https://countriesnow.space/api/v0.1/countries/population')
    .then(response => {
      info.value = response.data
    })
}

const getCountries = async () => {
  await axios.get('https://countriesnow.space/api/v0.1/countries/population')
    .then(response => {
      countries.value = response.data.data[0].country
    })
}
</script>

<style scoped>
    p {
        width: 300px;
    }
</style>