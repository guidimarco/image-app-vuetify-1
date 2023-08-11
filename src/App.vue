<script setup>
import { ref } from 'vue'

import SideBar from '@/components/SideBar.vue'
import ImageGallery from '@/components/ImageGallery.vue'

const isWithColor = ref(true)

const onSelectOption = (isColor) => {
  isWithColor.value = isColor
}
</script>

<template>
  <v-app>
    <side-bar @select-option="onSelectOption" />
    <v-main>
      <image-gallery :is-with-color="isWithColor" />
    </v-main>
  </v-app>
</template>

