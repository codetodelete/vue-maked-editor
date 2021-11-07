<template>
  <div id="md-editor">
    <textarea v-model="html"></textarea>
    <div v-html="compiledMarkdown"></div>
  </div>
</template>

<script>
import { marked } from 'marked';

export default {
  data () {
    return {
      html: "# hello markdown"
    }
  },
  computed: {
    compiledMarkdown() {
      return marked(this.html);
    }
  }
}
</script>

<style>
#md-editor {
  margin: 0;
  height: 100%;
}

textarea,
#md-editor div {
  display: inline-block;
  width: 49%;
  height: 100%;
  vertical-align: top;
  box-sizing: border-box;
  padding: 0 20px;
  margin: 5px;
  border: 1px solid #ccc;
  overflow: auto;
}

textarea {
  resize: none;
  font-size: 14px;
  padding: 20px;
}

code {
  color: #f66;
}
</style>