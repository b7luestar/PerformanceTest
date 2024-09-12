<script setup lang="ts">
import { ref, onMounted } from 'vue';

const timer = ref(0);
const stringArray = ref([] as string[]);
const counter = ref(0);

const createTimer = () => {
  timer.value = setInterval(() => {
    console.log('Timer running!');
    for (let i = 0; i < 500; i++) {
      stringArray.value.push('Timer running: ' + counter.value++);
    }
  }, 500);
}
const clearTimers = () => {
  clearInterval(timer.value);
}

onMounted(() => {
  createTimer();
});


</script>

<template>
  <div class="mt-3">
    <div class="btn m-2 btn-primary" @click="clearTimers">Clear Timers</div>
  </div> 
</template>