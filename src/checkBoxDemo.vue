<template>
  <i-checkbox v-model="single">单独选项</i-checkbox>
</template>
<script>
import iCheckbox from './components/checkBox/checkBox';
export default {
  components: {
    iCheckbox
  },
  data () {
    return {
      single: false
    }
  }
}
</script>
