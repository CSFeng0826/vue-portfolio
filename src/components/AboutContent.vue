<template>
  <v-parallax class="h-screen">
    <v-container class="px-4 pb-4 h-100" style="padding-top: 76px">
      <v-row class="h-100" no-gutters align="center" justify="center">
        <v-col cols="6">
          <Transition name="trans-card" appear>
            <v-card
              class="w-25 card elevation-20 pa-2"
              :style="{ top: cardTop + 'px', left: cardLeft + 'px' }"
            >
              <v-card-item>
                <v-card-title>
                  <span class="text-h4" style="font-weight: bold">Hi There,</span>
                  <br />
                  <span class="text-h2" style="font-weight: bold; line-height: 72px"
                    >I'm Vito Feng</span
                  >
                </v-card-title>
                <v-divider class="w-75 mt-2 mb-3" thickness="4"></v-divider>
                <v-card-subtitle class="text-h4" style="line-height: 32px">
                  A Web Developer
                </v-card-subtitle>
              </v-card-item>
            </v-card>
          </Transition>
          <div style="margin-top: 70%; margin-left: 20%">
            <v-btn size="x-large" class="bg-grey mr-5" color="white" icon="mdi-github"></v-btn>
            <v-btn size="x-large" class="bg-grey mr-5" color="white" icon="mdi-github"></v-btn>
            <v-btn size="x-large" class="bg-grey mr-5" color="white" icon="mdi-github"></v-btn>
            <v-btn size="x-large" class="bg-grey mr-5" color="white" icon="mdi-github"></v-btn>
            <v-btn size="x-large" class="bg-grey" color="white" icon="mdi-github"></v-btn>
          </div>
        </v-col>
        <v-col cols="6">
          <Transition name="trans-img" appear>
            <v-img width="552px" cover src="src/assets/img/S__48545795.jpg"></v-img>
          </Transition>
        </v-col>
      </v-row>
    </v-container>
  </v-parallax>
</template>
<script setup lang="ts">
let cardTop = 200
let cardLeft = 500
</script>
<style>
.card {
  position: absolute;
  z-index: 1;
}

.trans-card-enter-from {
  transform: translateX(-100%);
  opacity: 0;
}

.trans-card-enter-active {
  transition: all 0.8s ease-in-out;
}

.trans-img-enter-from {
  opacity: 0;
}

.trans-img-enter-active {
  transition: all 0.8s ease-in-out;
}
</style>
