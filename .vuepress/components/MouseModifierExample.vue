<template>
  <div>
    <h2>MouseModifierExample</h2>
    <button @click.left="onClickLeft">
      left
    </button>
    <button @click.middle="onClickMiddle">
      middle
    </button>
    <button @click.right="onClickRight">
      right
    </button>
    <div>
      left:{{left}} / middle:{{middle}} / right:{{right}}
    </div>
  </div>
</template>

<script>
export default {
  name: 'MouseModifierExample',
  data() {
    return {
      left: 0,
      middle: 0,
      right: 0,
    }
  },
  methods: {
    onClickLeft() {
      this.left += 1
    },
    onClickMiddle(e) {
      e.preventDefault()
      this.middle += 1
    },
    onClickRight(e) {
      e.preventDefault()
      this.right += 1
    },
  }
}
</script>
