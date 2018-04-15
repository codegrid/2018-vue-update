<template>
  <div>
    <h2>WrapperComponentExample</h2>
    <InputComponent :text="inputValue" placeholder="input text" @input="onInput"/>
    {{inputValue}}
  </div>
</template>

<script>
import InputComponent from './InputComponent.vue'
export default {
  name: 'WrapperComponentExample',
  data() {
    return {
      inputValue: '',
    }
  },
  methods: {
    onInput(e) {
      this.inputValue = e.target.value
    }
  },
  components: {
    InputComponent,
  },
}
</script>
