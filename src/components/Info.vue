<template>
  <ul>
    <li v-for="info in infos" :key="info.id" class="m-xs-p-0-2">
      <a :href="info.link" rel="noopener" target="_blank">{{info.info}}</a>
    </li>
  </ul>
</template>

<script>
import { ref } from 'vue'
export default {
  name: 'Info',
  setup() {
    const infos = ref([
      {
        id: 1,
        info: 'mush.hakobian@mail.ru',
        link: 'mailto:mush.hakobian@mail.ru'
      }, {
        id: 2,
        info: '+374 (77/99) 687439',
        link: 'tel:+37499687439'
      }, {
        id: 3,
        info: 'Sari Tax, Erevan, Armenia',
        link: 'https://www.google.ru/maps/@40.158267,44.521146,18.25z'
      }, {
        id: 4,
        info: 'facebook.com/mushakobian',
        link: 'https://www.facebook.com/mushakobian'
      }, {
        id: 5,
        info: 'github.com/MushHakobyan',
        link: 'https://github.com/MushHakobyan'
      }, {
        id: 6,
        info: 'linkedin.com/mush-hakobian',
        link: 'https://www.linkedin.com/in/mush-hakobian-b913611b7'
      }
    ])
    return { infos }
  }
}
</script>