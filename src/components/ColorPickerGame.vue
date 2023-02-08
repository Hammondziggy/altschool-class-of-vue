<template>
  <h1>Color Picker Game</h1>

  <div>{{ message }}</div>

  <button v-for="(color, index) in colors" :key="index" @click="matchColor(color)">
    {{ color }}
  </button>
</template>

<script>
import ColorManager from "../composables/ColorPickerComposable"

export default {
  setup() {
    const { colors, message, matchColor } = ColorManager();
    return { colors, message, matchColor } 
  }
};
</script>