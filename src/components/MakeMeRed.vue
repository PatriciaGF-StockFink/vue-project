<script setup>
import { ref } from 'vue'

const titleClass = ref('title')
const input = ref("")

// function updateColor() {
//   document.documentElement.style.setProperty('--title-color', input.value)
// }
</script>

<template>
  <div class="column">
    <!-- <h1 :class="titleClass">Make me red</h1> -->
    <h1 :style="`color: ${input}`">Make me red</h1>
  	<input v-model="input" type=text/>
    <p v-if="input">Well done!</p>
    <p v-else>Type a color</p>
  </div>
</template>

<style>
.title {
  color: var(--title-color, black)
}
</style>