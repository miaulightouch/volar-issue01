<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <HelloWorld msg="Welcome to Your Vue.js + TypeScript App"/>
  <span>{{ arr }}</span>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import HelloWorld from './components/HelloWorld.vue';
import { union } from 'lodash-es';

export default defineComponent({
  name: 'App',
  components: {
    HelloWorld
  },
  setup() {
    return {
      arr: union([1,1,1,1,1,1,2,2,1,1,1,3,3,3,4]),
    }
  },
});
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
