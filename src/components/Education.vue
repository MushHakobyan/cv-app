<template>
  <h2 class="m-ml-1">EDUCATION</h2>
  <div class="m-content m-pt-0 m-p-1">
      <div class="before after m-pl-2 m-relative" v-for="edu in education" :key="edu.id">
        <h3 class="m-mb-0">{{edu.title}}</h3>
        <h3 class="m-fw-400 m-m-0">{{edu.where}}</h3>
        <div class="m-text-primary m-d-flex m-jc-between">
          <i>{{edu.date}}</i>
          <i>{{edu.city}}</i>
        </div>
      </div>
  </div>
</template>

<script setup>
import { ref } from 'vue'
const education = ref([
  {
    id: 1,
    title: 'Mathematical Simulator',
    where: 'Armenian State University of Economics',
    date: '09/2012 - 05/2018',
    city: 'Erevan'
  }, {
    id: 2,
    title: 'Front End Development',
    where: 'Basic It Center',
    date: '05/2019 - 12/2019',
    city: 'Erevan'
  }, {
    id: 3,
    title: 'Web Development',
    where: 'Matemat',
    date: '12/2019 - 03/2020',
    city: 'Erevan'
  }
])
</script>