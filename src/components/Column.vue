<script setup>
const props = defineProps(['tasks']);

function addTask() {
  props.tasks.push('Raul');
}
</script>
<template>
  <div class="col bg-info">
    <header class="d-flex m-2">
      <i class="bi bi-list"></i>
      <h6 class="flex-grow-1">To do</h6>
      <i class="bi bi-three-dots"></i>
    </header>
    <div class="d-flex flex-column">
      <div v-for="task in tasks" class="fw-bold bg-white mx-2 mb-2 p-2">
        {{ task }}
      </div>
      <div
        @click="addTask"
        class="fw-bold bg-white mx-2 mb-2 d-flex justify-content-center p-2"
      >
        +Add Task
      </div>
    </div>
  </div>
</template>
