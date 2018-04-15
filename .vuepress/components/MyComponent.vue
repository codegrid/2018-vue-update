<template>
  <div>
    <input type="text" :value="text" @input="onInput">
  </div>
</template>

<script>
export default {
  name: 'MyComponent',
  props: {
    text: {
      type: String
    }
  },
  methods: {
    onInput(e) {
      const value = e.target.value
      this.$emit('update:text', value)
    },
  }
}
</script>
