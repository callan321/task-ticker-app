<!-- src/components/side-menu-bar/SideMenuBar.vue -->
<template>
  <div class="flex flex-col w-14 h-screen py-4 bg-gray-50 border-gray-300 border-r-2 shadow-md">
    <!-- Top Section -->
    <div class="flex flex-col items-center space-y-8">
      <!-- Tab Button -->
      <IconButton icon="menu" @click="toggleSidebar" />
    </div>

    <!-- Divider Line -->
    <DividerLine />

    <!-- Middle Section (flex-grow) -->
    <div class="flex flex-col items-center space-y-2 flex-grow">
      <!-- Home Button -->
      <router-link to="/">
        <IconButton icon="home" />
      </router-link>
      <!-- Settings Button -->
      <IconButton icon="dark_mode" />
    </div>

    <!-- Divider Line -->
    <DividerLine />

    <!-- Bottom Section -->
    <div class="flex flex-col items-center space-y-4">
      <IconButton icon="person" />
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue'
import IconButton from './IconButton.vue'
import DividerLine from './DividerLine.vue'
import { useSidebarStore } from '@/stores/sidebar'

export default defineComponent({
  name: 'SideMenuBar',
  components: {
    IconButton,
    DividerLine
  },
  setup() {
    const sidebarStore = useSidebarStore()

    const toggleSidebar = () => {
      sidebarStore.toggleSidebar()
    }

    return {
      toggleSidebar
    }
  }
})
</script>
