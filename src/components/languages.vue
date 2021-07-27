<template>
    <h2 class="m-ml-1">LANGUAGES</h2>
    <div class="m-content m-p-1 m-d-grid m-g-gap-1 m-gt-columns-2">
        <div v-for="lang in langs" :key="lang.id">
        <h3 class="m-m-0">{{lang.name}}</h3>
        <i class="m-text-primary">{{lang.level}}</i>
        </div>
    </div>
</template>

<script>
import { ref } from 'vue'
export default {
  name: 'Languages',
  setup() {
    const langs = ref([
      {
        id: 1,
        name: 'Armenian',
        level: 'Full Professional Proficiency',
      }, {
        id: 2,
        name: 'English',
        level: 'Professional Working Proficiency'
      }, {
        id: 3,
        name: 'Russian',
        level: 'Limited Working Proficiency'
      }
    ])
    return { langs }
  }
}
</script>