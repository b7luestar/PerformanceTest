<script setup lang="ts">
import Timer from './components/Timer.vue'
import EventHandler from './components/EventHandler.vue';

import { ref } from 'vue';
const toggleTimer = ref(false);

const toggleTimerComponent = () => {
  toggleTimer.value = !toggleTimer.value;
}

const toggleEventhandler = ref(false);
const toggleEventHandlerComponent = () => {
  toggleEventhandler.value = !toggleEventhandler.value;
}
</script>

<template>
  <div class="d-flex flex-column">
    <div class="btn btn-primary" @click="toggleTimerComponent">{{ toggleTimer? "Delete": "Create" }} Timer component</div>
    <div class="btn btn-primary mt-2" @click="toggleEventHandlerComponent">{{ toggleEventhandler? "Delete": "Create" }} Event Handler component</div>
  </div>
  <Timer v-if="toggleTimer"/>
  <EventHandler v-if="toggleEventhandler"/>
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
