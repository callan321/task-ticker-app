<!-- src/views/EditorView.vue -->
<template>
  <div class="flex flex-row h-screen overflow-hidden">
    <!-- Main Menu Bar -->
    <SideMenuBar />
    <!-- Side Bar (optional) -->
    <SideBarDiv v-if="isSidebarOpen" />
    <!-- Main Viewport -->
    <div class="flex flex-col flex-grow bg-gray-25">
      <div class="flex w-full h-16 border border-w">
        <!-- Topbar -->
      </div>
      <div class="flex-grow h-full w-full overflow-y-auto overflow-x-hidden">
        <TextEditor />
      </div>
    </div>
  </div>
</template>
<script lang="ts">
import { defineComponent, computed } from 'vue'
import { useSidebarStore } from '../stores/sidebar'
import SideMenuBar from '../components/side-menu-bar/SideMenuBar.vue'
import SideBarDiv from '../components/side-bar/SideBarDiv.vue'
import TextEditor from '../components/text-editor/TextEditor.vue'

export default defineComponent({
  name: 'EditorView',
  components: {
    SideMenuBar,
    SideBarDiv,
    TextEditor
  },
  setup() {
    const sidebarStore = useSidebarStore()

    const isSidebarOpen = computed(() => sidebarStore.isSidebarOpen)

    return {
      isSidebarOpen
    }
  }
})
</script>
