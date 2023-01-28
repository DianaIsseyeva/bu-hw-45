<template>
  <div>
    <label for=""> {{ label }}
      <input
        :value="modelValue"
        @input="input"
      />
    </label>
  </div>
</template>

<script>
 export default {
  name: 'v-input',
  props: {
    modelValue: {
      type: [String, Number],
      default: '',
    },
   label: {
      type: String,
      default: '',
   }
 },
  emits: ['update:modelValue'],
  data() {
    return {}
  },
  methods: {
    input(e) {
      let value = e.target.value;
      this.$emit('update:modelValue', value)
    }
  }
 }
</script>

<style>

</style>