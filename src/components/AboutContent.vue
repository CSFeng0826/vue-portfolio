<template>
  <v-parallax class="h-screen">
    <v-container class="px-4 pb-4 h-100" style="padding-top: 76px">
      <v-row class="h-100" no-gutters align="center" justify="center">
        <v-col cols="12">
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
          <Transition name="trans-btn" appear>
            <v-card
              class="d-flex w-25 elevation-20 pa-5 justify-end"
              style="position: absolute; top: 70%; right: 15%"
            >
              <Transition
                name="trans-btn"
                :style="{ 'transition-delay': (icon_list.length - 1 - index) * 0.1 + 's' }"
                style="z-index: 0"
                v-for="(icon_name, index) in icon_list"
                :key="index"
                appear
              >
                <v-btn
                  size="x-large"
                  class="bg-grey"
                  :class="index != icon_list.length - 1 ? 'mr-5' : ''"
                  color="white"
                  :icon="icon_name"
                ></v-btn>
              </Transition>
            </v-card>
          </Transition>
        </v-col>
        <v-img
          width="552px"
          cover
          src="src/assets/img/S__48545795.jpg"
          style="position: absolute; z-index: 1"
        ></v-img>
        <v-sheet class="w-30" style="position: absolute; top: 30%; right: 5%; font-size: 16px">
          <span class="ml-3" style="font-size: 28px"><b>About me</b></span>
          <v-divider class="w-50 mt-2 ml-3" thickness="4"></v-divider>
          <v-list>
            <v-list-item> Familiar with both front-end and back-end development </v-list-item>
            <v-list-item>
              Committed to creating high-quality websites and applications
            </v-list-item>
            <v-list-item> Emphasizing user experience and technological innovation </v-list-item>
            <v-list-item> Enjoy learning emerging technologies </v-list-item>
          </v-list>
        </v-sheet>
      </v-row>
    </v-container>
  </v-parallax>
</template>
<script setup lang="ts">
let cardTop = 200
let cardLeft = 200

const icon_list = [
  'mdi:mdi-github',
  'mdi:mdi-linkedin',
  'mdi:mdi-instagram',
  'fa-brands fa-telegram'
]
</script>
<style>
.card {
  position: absolute;
  z-index: 2;
}

.trans-card-enter-from {
  /* transform: translateX(-100%); */
  opacity: 0;
}

.trans-card-enter-active {
  transition: all 0.8s ease-in-out;
}

.trans-btn-enter-from {
  transform: translateX(-200px);
  opacity: 0;
}

.trans-btn-enter-active {
  transition: all 0.8s ease-in-out;
}
</style>
