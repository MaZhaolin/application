<template>
  <div class="ft-modal" :style="{display: visible ? 'block' : 'none'}">
    <div class="ft-modal-content" >
      <div class="ft-modal-header">
        <slot name="title">Save you work?</slot>
      </div>
      <div class="ft-modal-body">
        <slot name="body"></slot>
      </div>
      <slot name="footer"></slot>
    </div>
    <div class="ft-modal-mask"></div>
  </div>
</template>

<script>
export default {
  props: {
    visible: {
      type: Boolean,
      default: false
    }
  }
}
</script>
