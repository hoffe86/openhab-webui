<template>
  <rule-picker :title="configDescription.label" :value="value" @input="updateValue" :multiple="configDescription.multiple" :required="configDescription.required" />
</template>

<script>
import RulePicker from './rule-picker.vue'

export default {
  props: ['configDescription', 'value'],
  components: {
    RulePicker
  },
  methods: {
    updateValue (value) {
      this.$emit('input', value)
    }
  }
}
</script>
