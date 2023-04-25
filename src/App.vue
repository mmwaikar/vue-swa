<template>
  <HelloWorld />

  <p></p>
  <div><a v-bind:href="swaUrl">Azure static web apps</a> with <a v-bind:href="vueUrl">Vue.js</a> are amazing!</div>

  <p></p>
  <ListCountries />
</template>

<script>
import HelloWorld from './components/HelloWorld.vue';
import ListCountries from './components/ListCountries.vue';

export default {
    name: "App",
    data() {
        return {
            swaUrl: "https://azure.microsoft.com/en-in/products/app-service/static/",
            vueUrl: "https://vuejs.org/"
        };
    },
    components: { HelloWorld, ListCountries }
};
</script>
