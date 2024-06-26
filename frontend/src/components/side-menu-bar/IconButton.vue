<template>
  <button
    class="flex items-center justify-center w-12 h-12 bg-gray-200 hover:bg-gray-300 rounded-full hover:shadow-md text-black"
    @click="handleClick"
  >
    <span class="material-icons">{{ icon }}</span>
  </button>
</template>

<script lang="ts">
import { defineComponent } from 'vue'

export default defineComponent({
  name: 'MyButton',
  props: {
    icon: {
      type: String,
      required: true
    }
  }
})
</script>
