<template>
  <HelloWorld />

  <p></p>
  <div><a v-bind:href="swaUrl">Azure static web apps</a> with <a v-bind:href="vueUrl">Vue.js</a> are amazing!</div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue';

export default {
    name: "App",
    data() {
        return {
            swaUrl: "https://azure.microsoft.com/en-in/products/app-service/static/",
            vueUrl: "https://vuejs.org/"
        };
    },
    components: { HelloWorld }
};
</script>
