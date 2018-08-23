<template>
  <div id="app">
    <div class="header">
      <ft-icon code="E703"></ft-icon>
    </div>
    <FtButton @click.native="() => visible = true">show modal</FtButton>
    <FtSwitch></FtSwitch>
    <FtModal :visible="visible">
      <div slot="title">Save your work?</div>
      <div slot="body">
        Lorem, ipsum dolor sit amet consectetur adipisicing elit. Vitae ab nam vel velit. Doloremque cumque eius ab architecto voluptas odio, natus sunt quos commodi amet accusantium, quam placeat ratione necessitatibus?
      </div>
      <div slot="footer">
        <FtButton type="primary" @click.native="() => visible = false">Button</FtButton>
        <ft-button>Cancel</ft-button>
      </div>
    </FtModal>
    Hello,World
    <!-- <landing-page></landing-page> -->
  </div>
</template>

<script>
  import FtIcon from './components/icon'
  import FtButton from './components/button'
  import FtSwitch from './components/switch'
  import FtModal from './components/modal'
  export default {
    name: 'application',
    data () {
      return {
        visible: true
      }
    },
    components: {
      FtIcon,
      FtButton,
      FtSwitch,
      FtModal
    }
  }
</script>

<style>
.header {
  -webkit-app-region: drag;
  height: 60px;
  background: orange 
}
  /* CSS */
</style>
