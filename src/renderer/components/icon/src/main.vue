<template>
  <!-- eslint-disable-next-line vue/no-parsing-error -->
  <i class="ft-icon" v-html="`&#x${code};`" :style="{color, fontSize: `${size}px`}"></i> 
</template>

<script>
export default {
  props: {
    color: {
      type: String,
      default: '#000'
    },
    code: {
      type: String
    },
    size: {
      type: Number,
      default: 32
    }
  }
}
</script>
