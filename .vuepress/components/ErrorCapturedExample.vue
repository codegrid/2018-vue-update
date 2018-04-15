<template>
  <div>
    <h2>ErrorCapturedExample</h2>
    <ErrorComponent v-if="!isError"/>
    <div v-else>
      <h2>
        Error!!
      </h2>
      {{errorMessage}}
    </div>
  </div>
</template>

<script>
import ErrorComponent from './ErrorComponent.vue'
export default {
  name: 'ErrorCapturedExample',
  data() {
    return {
      isError: false,
      errorMessage: '',
    }
  },
  errorCaptured(err) {
    this.isError = true
    this.errorMessage = err.message
    return false
  },
  components: {
    ErrorComponent,
  }
}
</script>
