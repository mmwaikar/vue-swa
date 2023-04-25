<template>
    <div>List of countries</div>
    <ul v-if="countries">
        <li v-for="country in countries" :key="country.id">
            {{ country.name }}
        </li>
    </ul>
</template>
  
<script setup>
import { ref, onMounted } from "vue";

const countries = ref(null)

async function fetchCountries() {
    const response = await fetch('/data-api/api/Country')
    const jsonData = await response.json();

    console.log(`countries`, jsonData)
    countries.value = jsonData.value
}

onMounted(() => {
    fetchCountries()
})
</script>
  