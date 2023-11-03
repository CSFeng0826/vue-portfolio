<template>
  <v-app-bar color="white" height="60">
    <v-app-bar-nav-icon>
      <v-icon size="50px" color="text-yellow" icon="mdi-alpha-v-box-outline"></v-icon>
    </v-app-bar-nav-icon>
    <v-app-bar-title class="w-25">Portfolio</v-app-bar-title>
    <div class="w-25 d-inline-flex justify-space-between">
      <v-btn
        v-for="(item, index) in sectionList"
        @click="scrollToElement(item, index)"
        :key="index"
      >
        {{ item }}
      </v-btn>
    </div>
    <v-spacer></v-spacer>
    <v-btn>TEST6</v-btn>
  </v-app-bar>
</template>
<script setup lang="ts">
import { defineEmits } from 'vue'
const sectionList = ['About', 'Skills', 'Education', 'Experience', 'Contact']

const emits = defineEmits(['scrollToElement'])

function scrollToElement(item: string, index: number) {
  emits('scrollToElement', { item: item, index: index })
}
</script>
