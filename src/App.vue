<template>
  <div id="app">
    <h1 class="title">vue-markdown-editor</h1>
    <MarkedEditor/>
  </div>
</template>

<script>
import MarkedEditor from './components/MarkedEditor'

export default {
  name: 'App',
  components: {
    MarkedEditor
  }
}
</script>

<style>
html,
body,
#app {
  height: 100%;
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}
.title {
  text-align: center;
}
</style>
