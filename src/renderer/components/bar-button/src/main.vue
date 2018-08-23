<template>
  <button class="ft-bar-button">
    <icon :code="this.icon" :size="size"></icon>
    <span class="ft-bar-button--label">{{label}}</span>
  </button>
</template>

<script>
import icon from '../../icon'
// const prefixClass = 'ft-button'

export default {
  props: {
    icon: {
      type: String,
      default: 'default'
    },
    size: {
      type: Number,
      default: 10
    },
    label: {
      type: String,
      default: ''
    }
  },
  components: {
    icon
  }
}
</script>
