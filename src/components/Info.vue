<template>
  <ul>
    <li v-for="info in infos" :key="info.id">
      <a :href="info.link" target="_blank">{{info.info}}</a>
      <span class="m-icon m-jc-center m-ml-0-5"><i :class="info.icon" class="m-text-shadow m-text-primary"></i></span>
    </li>
  </ul>
</template>

<script setup>
import { ref } from 'vue'
const infos = ref([
  {
    id: 1,
    info: 'mush.hakobian@mail.ru',
    icon: 'fas fa-envelope',
    link: 'mailto:mush.hakobian@mail.ru'
  }, {
    id: 2,
    info: '+374 (77/99) 687439',
    icon: 'fas fa-mobile-alt',
    link: 'tel:+37499687439'
  }, {
    id: 3,
    info: 'Sari Tax, Erevan, Armenia',
    icon: 'fas fa-map-marker-alt',
    link: 'https://www.google.ru/maps/@40.158267,44.521146,18.25z'
  }, {
    id: 4,
    info: 'facebook.com/mushakobian',
    icon: 'fab fa-facebook-f',
    link: 'https://www.facebook.com/mushakobian'
  }, {
    id: 5,
    info: 'github.com/MushHakobyan',
    icon: 'fab fa-github',
    link: 'https://github.com/MushHakobyan'
  }, {
    id: 6,
    info: 'linkedin.com/mush-hakobian',
    icon: 'fab fa-linkedin-in',
    link: 'https://www.linkedin.com/in/mush-hakobian-b913611b7'
  }
])
</script>