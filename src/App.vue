<template>
  <div class="container m-shadow m-pb-1 m-mx-auto m-my-2 m-xs-m-0" ref="container" @mousemove="rotate" @mouseleave="none">
    <div class="m-d-flex m-jc-between m-p-2 m-xs-fd-column">
      <div class="m-avatar-content m-d-flex m-xs-fd-column m-xs-ai-center">
        <Avatar />
      </div>
      <div class="m-info-content m-text-right m-xs-text-center">
        <Info />
        <div class="m-xs-d-none">
          <input type="checkbox" id="input" v-model="effect3d">
          <label for="input" class="m-pr-1-5 m-relative">Turn {{effect3d ? 'off' : 'on'}} 3d effect</label>
        </div>
      </div>
    </div>
    <div class="m-d-flex m-xs-fd-column">
      <div class="m-mw-50 m-mr-1 m-xs-m-0">
        <Experience />
        <Education />
      </div>
      <div class="m-fg-1 m-ml-1 m-xs-m-0">
        <Skills />
        <Languages />
        <Interests />
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue'
import Avatar from './components/Avatar.vue'
import Education from './components/Education.vue'
import Experience from './components/Experience.vue'
import Info from './components/Info.vue'
import Interests from './components/Interests.vue'
import Skills from './components/Skills.vue'
import Languages from './components/languages.vue'
const effect3d = ref(false)
const container = ref(null)
function rotate(e) {
  if (effect3d.value) {
    container.value.style.transform = `rotateX(${(innerHeight/2-e.y)/20}deg) rotateY(${(e.x-innerWidth/2)/20}deg)`;
  } else {  container.value.style.transform = 'none' }
}
function none() { container.value.style.transform = 'none' }
</script>
