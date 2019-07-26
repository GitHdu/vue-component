<template>
  <div>
    <i-checkbox-group v-model="multiple">
      <i-checkbox label="option1">选项 1</i-checkbox>
      <i-checkbox label="option2">选项 2</i-checkbox>
      <i-checkbox label="option3">选项 3</i-checkbox>
      <i-checkbox label="option4">选项 4</i-checkbox>
    </i-checkbox-group>
  </div>
</template>
<script>
import iCheckboxGroup from './components/checkBox/checkBoxGroup'
import iCheckbox from './components/checkBox/checkBox'
export default {
  components: {
    iCheckboxGroup,
    iCheckbox
  },
  data () {
    return {
      multiple: ['option1', 'option3']
    }
  }
}
</script>
