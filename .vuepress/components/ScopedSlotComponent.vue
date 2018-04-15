<template>
  <div>
    <slot
      v-for="item in items"
      :id="item.id"
      :text="item.text"
    />
  </div>
</template>

<script>
export default {
  name: 'ScopedSlotComponent',
  props: {
    items: Array,
  },
}
</script>
