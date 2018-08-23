<template>
  <span :class="['ft-switch', isActive ? 'active' : '']" @click="toggle"></span>
</template>

<script>
export default {
  data () {
    return {
      isActive: false
    }
  },
  methods: {
    toggle () {
      this.isActive = !this.isActive
    }
  }
}
</script>

