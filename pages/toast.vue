<template>
  <div id="editor"></div>
</template>

<script>
import Editor from '@toast-ui/editor';
import '@toast-ui/editor/dist/toastui-editor.css'; // Editor's Style

export default{
  data(){
    return {
      editor: null  
    }
  },
  mounted(){
    this.editor = new Editor({
      el: document.querySelector('#editor'),
      height: '500px',
      initialEditType: 'markdown',
      previewStyle: 'vertical'
    });
  },
}
</script>

<style lang="scss" scoped>

</style>