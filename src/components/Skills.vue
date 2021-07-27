<template>
    <h2 class="m-ml-1">SKILLS</h2>
    <div class="m-content m-p-1 m-d-flex m-f-wrap">
        <span v-for="skill in skills" :key="skill.id" class="m-shadow m-text-white m-fw-500 m-bg-primary m-py-0-25 m-px-0-5 m-mr-0-5 m-mb-0-5 m-radius-0-25 m-uppercase">{{skill.name}}</span>
    </div>
</template>
<script>
import { ref } from 'vue'
export default {
  name: 'Skils',
  setup() {
    const skills = ref([
      {
        id: 1,
        name: 'HTML5',
      }, {
        id: 2,
        name: 'CSS3',
      }, {
        id: 3,
        name: 'Bulma',
      }, {
        id: 4,
        name: 'JavaScript',
      }, {
        id: 5,
        name: 'Vue JS',
      }, {
        id: 6,
        name: 'Vue Router',
      }, {
        id: 7,
        name: 'Vuex',
      }, {
        id: 8,
        name: 'Nuxt JS',
      }, {
        id: 9,
        name: 'Express JS',
      }, {
        id: 10,
        name: 'Node JS',
      }
    ])
    return { skills }
  }
}
</script>