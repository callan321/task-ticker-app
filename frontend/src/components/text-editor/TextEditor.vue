<template>
  <div class="flex justify-center items-start py-24 px-16 h-full bg-inherit">
    <div class="box-border w-3/5 flex">
      <div class="prose-lg font-mono">
        <editor-content :editor="editor" />
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import { onMounted, onBeforeUnmount, defineComponent } from 'vue'
import { EditorContent, useEditor } from '@tiptap/vue-3'
import StarterKit from '@tiptap/starter-kit'

export default defineComponent({
  name: 'MarkdownEditor',
  components: {
    EditorContent
  },
  setup() {
    const editor = useEditor({
      extensions: [
        StarterKit.configure({
          heading: {
            levels: [1, 2, 3]
          }
        })
      ],
      content: '<h1>Untitled</h1>',
      editorProps: {
        attributes: {
          class: 'prose prose-lg markdown-body',
          style: 'outline: none;'
        }
      }
    })

    onMounted(() => {
      if (editor.value) {
        editor.value.commands.focus('end')
      }
    })

    onBeforeUnmount(() => {
      if (editor.value) {
        editor.value.destroy()
      }
    })

    return {
      editor
    }
  }
})
</script>
