<script setup>
import AddColumn from '../components/AddColumn.vue';
import Column from '../components/Column.vue';

import { ref } from 'vue';

function addColumn() {
  columns.value.push(['Daniel']);
}

const columns = ref([]);
</script>

<template>
  <h2 class="m-4">Kanban</h2>

  <div class="container-fluid">
    <div class="row gap-3">
      <Column v-for="column in columns" :tasks="column" />
      <AddColumn @add-column="addColumn" />
    </div>
  </div>
</template>
