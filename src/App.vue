<template>
  <v-app>
    <header>
      <ToolBar @scrollToElement="scrollToElement" />
    </header>
    <main>
      <component
        :is="component"
        ref="sections"
        v-for="(component, index) in components"
        :key="index"
      >
      </component>
    </main>
  </v-app>
</template>

<script setup lang="ts">
import { ref } from 'vue'
import ToolBar from './components/ToolBar.vue'
import AboutContent from './components/AboutContent.vue'
import ContactContent from './components/ContactContent.vue'
import EducationContent from './components/EducationContent.vue'
import ExperienceContent from './components/ExperienceContent.vue'
import SkillContent from './components/SkillContent.vue'

const sections = ref([])
const components = [AboutContent, SkillContent, EducationContent, ExperienceContent, ContactContent]

function scrollToElement(val: { item: string; index: number }) {
  ;(sections.value[val.index] as any)?.$el.scrollIntoView({ behavior: 'smooth', block: 'start' })
}
</script>

<style scoped>
* {
  font-family: 'Montserrat';
}
</style>
