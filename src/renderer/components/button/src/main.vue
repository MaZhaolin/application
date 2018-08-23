<template>
  <button :class="['ft-button', btnClass]">
    <slot></slot>
  </button>
</template>

<script>
const prefixClass = 'ft-button'

export default {
  props: {
    type: {
      type: String,
      default: 'default'
    }
  },
  computed: {
    btnClass () {
      return `${prefixClass}-${this.type}`
    }
  }
}
</script>
