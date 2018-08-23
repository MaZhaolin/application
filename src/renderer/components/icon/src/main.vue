<template>
  <i class="ft-icon" v-html="`&#x${code};`" :style="{color}"></i> 
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
    }
  }
}
</script>
