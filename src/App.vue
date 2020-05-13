<template>
  <div id="app">
    <botMediaTest :one="1" :two="2" ref="test"/>
    <button v-on:click="asdf">Increment</button>
  </div>
</template>

<script>
import botMediaTest from "./components/botMediaTest.vue";

export default {
    name: "App",
    components: {
        botMediaTest
    },
    methods: {
        asdf() {
            this.$refs.test.increment();
        }
    }
};
</script>
