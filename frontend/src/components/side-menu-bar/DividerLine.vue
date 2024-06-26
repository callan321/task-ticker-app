<!-- src/components/side-bar/DividerLine.vue -->
<template>
  <div
    :class="['w-3/4 mx-auto border-t border-2 border-gray-300 my-4 shadow-sm', customClass]"
  ></div>
</template>

<script lang="ts">
import { defineComponent, PropType } from 'vue'

export default defineComponent({
  name: 'DividerLine',
  props: {
    customClass: {
      type: String,
      default: ''
    }
  }
})
</script>
