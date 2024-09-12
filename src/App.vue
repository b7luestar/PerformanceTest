<script setup lang="ts">
import HelloWorld from './components/HelloWorld.vue'

import { ref } from 'vue';
const toggle = ref(false);

const toggleTimerComponent = () => {
  toggle.value = !toggle.value;
}

</script>

<template>
  <div>
    <div class="btn btn-primary" @click="toggleTimerComponent">{{ toggle? "Delete": "Create" }} Timer component</div>
  </div>
  <HelloWorld v-if="toggle"/>
</template>

<style scoped>
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
  transition: filter 300ms;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}
.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}

</style>
