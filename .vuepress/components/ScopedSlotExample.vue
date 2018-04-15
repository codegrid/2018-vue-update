<template>
  <div>
    <h2>ScopedSlotExample</h2>
    <ScopedSlotComponent :items="items">
      <div slot-scope="scopedProps">
        {{scopedProps.id}}/{{scopedProps.text}}
      </div>
    </ScopedSlotComponent>
  </div>
</template>

<script>
import ScopedSlotComponent from './ScopedSlotComponent.vue'
export default {
  data() {
    return {
      items: [
        {
          id: 1,
          text: 'sugoi text',
        },
        {
          id: 2,
          text: 'yabai text',
        },
      ]
    }
  },
  components: {
    ScopedSlotComponent,
  },
}
</script>
