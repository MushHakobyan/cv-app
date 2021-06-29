<template>
    <h2 class="m-ml-1">INTERESTS</h2>
    <div class="m-content m-p-1 m-d-flex m-f-wrap">
        <span v-for="interest in interests" :key="interest.id" class="m-shadow m-fw-500 m-py-0-25 m-px-0-5 m-mr-0-5 m-mb-0-5 m-radius-0-25 m-uppercase m-border">{{interest.name}}</span>
    </div>
</template>

<script setup>
import { ref } from 'vue'
const interests = ref([
  {
    id: 1,
    name: 'Programming',
  }, {
    id: 2,
    name: 'Gaming',
  }, {
    id: 3,
    name: 'Personal development',
  }, {
    id: 4,
    name: 'Cooking',
  }
])
</script>