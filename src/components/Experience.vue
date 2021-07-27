<template>
    <h2 class="m-ml-1">EXPERIENCE</h2>
    <div class="m-content m-p-1 m-pt-0">
        <div class="before after m-pl-2 m-relative" v-for="exp in experience" :key="exp.id">
        <h3 class="m-mb-0">{{exp.title}}</h3>
        <h3 class="m-fw-400 m-m-0">{{exp.where}}</h3>
        <div class="m-text-primary m-d-flex m-jc-between">
            <i>{{exp.date}}</i>
            <i>{{exp.city}}</i>
        </div>
        </div>          
    </div>
</template>

<script>
import { ref } from 'vue'
export default {
  name: 'Experience',
  setup() {
    const experience = ref([
      {
        id: 1,
        title: 'Front-End Developer',
        where: 'Iguan Systems LLC',
        date: '02/2021 - now',
        city: 'Erevan'
      }
    ])
    return { experience }
  }
}
</script>