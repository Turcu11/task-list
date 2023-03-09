<script setup>
defineEmits(['addColumn']);
</script>
<template>
  <div class="col">
    <header
      @click="$emit('addColumn')"
      class="fw-bold d-flex justify-content-center p-2 m-2 bg-info"
    >
      +Add Column
    </header>
  </div>
</template>
