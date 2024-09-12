<script setup lang="ts">

const keyDownEventHandler = (e: KeyboardEvent) => {
  console.log('Key pressed:', e.key);
}

const addEventHandler = () => {
  window.addEventListener('keydown', keyDownEventHandler);
}

const clearEventHandler = () => {
  window.removeEventListener('keydown', keyDownEventHandler);
}

</script>

<template>
  <div class="mt-3">
    <h3>Event Handler</h3>
    <div class="btn btn-primary m-2" @click="addEventHandler">Add EventHandler</div>
    <div class="btn btn-primary m-2" @click="clearEventHandler">Clear EventHandler</div>
  </div> 
</template>