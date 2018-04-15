<template>
  <div>
    <h2>ErrorCaptured Example</h2>
    <ErrorComponent/>
  </div>
</template>

<script>
import ErrorComponent from './ErrorComponent.vue'
export default {
  name: 'RenderErrorExample',
  errorCaptured(e) {
    console.log(e)
  },
  components: {
    ErrorComponent,
  },
}
</script>
