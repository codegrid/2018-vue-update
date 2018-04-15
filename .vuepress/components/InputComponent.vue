<template>
  <div>
    <input type="text" :value="text" v-bind="$attrs" v-on="$listeners">
  </div>
</template>

<script>
export default {
  name: 'InputComponent',
  props: {
    text: String,
  },
  inheritAttrs: false,
}
</script>
