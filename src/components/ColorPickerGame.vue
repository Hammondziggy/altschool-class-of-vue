<template>
  <h1>Color Picker Game</h1>

  <div>{{ message }}</div>

  <button v-for="color in colors" :key="color" @click="matchColor(color)">
    {{ colors }}
  </button>
</template>

<script>
import colorManager from "../composables/ColorPickerComposable"

export default {
  setup() {
    return { colors, message, matchColor } = colorManager();
  },
};  
</script>
