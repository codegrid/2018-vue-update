<template>
  <div>
    <h2>VBindSyncExample</h2>
    <MyComponent :text.sync="message"/>
    {{message}}
  </div>
</template>

<script>
import MyComponent from './MyComponent.vue'
export default {
  name: 'VBindSyncExample',
  data() {
    return {
      message: 'hello',
    }
  },
  components: {
    MyComponent,
  }
}
</script>
