<template>
  <div>
    <h2>KeyModifierExample</h2>
    <div>
      <label>
        @click.shift
        <button @click.shift="onClick">click me</button>
      </label>
    </div>
    <div>
      <label>
        @click.shift.exact
        <button @click.shift.exact="onClick">click me</button>
      </label>
    </div>
    <div>
      <label>
        @click.exact
        <button @click.exact="onClick">click me</button>
      </label>
    </div>
    <div>
      <label>
        @keyup.shift.enter
        <input @keyup.shift.enter="onEnter">
      </label>
    </div>
  </div>
</template>

<script>
export default {
  name: 'KeyModifierComponent',
  methods: {
    onClick() {
      window.alert('onClick')
    },
    onEnter() {
      window.alert('onEnter')
    }
  },
}
</script>
