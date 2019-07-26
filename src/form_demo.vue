<template>
  <div>
    <i-form :model="formValidate"
            :rules="ruleValidate">
      <i-form-item label="用户名"
                   prop="name">
        <i-input v-model="formValidate.name"></i-input>
      </i-form-item>
      <i-form-item label="邮箱"
                   prop="mail">
        <i-input v-model="formValidate.mail"></i-input>
      </i-form-item>
      <i-form-item label="single"
                   prop="single">
        <i-checkbox v-model="formValidate.single">单独选项</i-checkbox>
      </i-form-item>
      <i-form-item label="multi"
                   prop="multi">
        <check-box-group-demo></check-box-group-demo>
      </i-form-item>
    </i-form>
  </div>
</template>
<script>
import iForm from './components/form/form.vue'
import iFormItem from './components/form/form-item.vue'
import iInput from './components/input/input.vue'
import iCheckbox from './components/checkBox/checkBox'
import checkBoxGroupDemo from './checkBoxGroupDemo'

export default {
  components: {
    iForm,
    iFormItem,
    iInput,
    iCheckbox,
    checkBoxGroupDemo
  },
  data () {
    return {
      formValidate: {
        name: '',
        mail: '',
        single: false
      },
      ruleValidate: {
        name: [
          { required: true, message: '用户名不能为空', trigger: 'blur' }
        ],
        mail: [
          { required: true, message: '邮箱不能为空', trigger: 'blur' },
          { type: 'email', message: '邮箱格式不正确', trigger: 'blur' }
        ],
        single: [
          { type: 'boolean', required: true, message: '请勾选', trigger: 'change', validator: (rule, value) => value === true }
        ]
      }
    }
  }
}
</script>
