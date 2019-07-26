<template>
  <div id="app">
    <form-demo />
    <i-display :code="code"></i-display>
  </div>
</template>

<script>
import formDemo from './form_demo'
import iDisplay from './components/display/display.vue'
import defaultCode from './default-code.js'

export default {
  name: 'app',
  components: {
    formDemo,
    iDisplay
  },
  data () {
    return {
      code: defaultCode
    }
  }
}
</script>

<style lang="less">
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
