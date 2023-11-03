<template>
  <v-app>
    <header>
      <ToolBar />
    </header>
    <main>
      <AboutContent />
      <SkillContent />
      <EducationContent />
      <ExperienceContent />
      <ContactContent />
    </main>
  </v-app>
</template>
<script setup lang="ts">
import ToolBar from './components/ToolBar.vue'
import AboutContent from './components/AboutContent.vue'
import ContactContent from './components/ContactContent.vue'
import EducationContent from './components/EducationContent.vue'
import ExperienceContent from './components/ExperienceContent.vue'
import SkillContent from './components/SkillContent.vue'

function scrollToElement(val: object) {
  console.log('test', val)
}
</script>
<style scoped></style>
