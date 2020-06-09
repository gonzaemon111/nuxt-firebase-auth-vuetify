<template>
  <div>
    <editor v-model="editorText" :options="editorOptions" :visible="editorVisible" height="500px" previewStyle="vertical" />
    <viewer :value="editorText" />
  </div>

</template>
<script>
  import {
    Editor,
    Viewer
  } from '@toast-ui/vue-editor'

  export default {
    components: {
      'editor': Editor,
      'viewer': Viewer
    },
    data() {
      return {
        editorText: '',
        editorOptions: {
          hideModeSwitch: true
        },
        editorVisible: true
      }
    }
  }
</script>
