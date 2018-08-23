<template>
  <div id="app">
    <div class="header">
      <div class="drag"></div>
      <FtBarButton icon="E921"></FtBarButton>
      <FtBarButton icon="E922"></FtBarButton>
      <FtBarButton icon="E8BB" @click.native="close"></FtBarButton>
    </div>
    <FtButton @click.native="() => visible = true">show modal</FtButton>
    <FtBarButton icon="E711" label="asdads"></FtBarButton>
    <FtSwitch></FtSwitch>
    <FtModal :visible="visible">
      <div slot="title">Save your work?</div>
      <div slot="body">
        Lorem, ipsum dolor sit amet consectetur adipisicing elit. Vitae ab nam vel velit. Doloremque cumque eius ab architecto voluptas odio, natus sunt quos commodi amet accusantium, quam placeat ratione necessitatibus?
      </div>
      <div slot="footer">
        <FtButton type="primary">Button</FtButton>
        <ft-button @click.native="() => visible = false">Cancel</ft-button>
      </div>
    </FtModal>
    Hello,World
    <!-- <landing-page></landing-page> -->
  </div>
</template>

<script>
  import FtIcon from './components/icon'
  import FtButton from './components/button'
  import FtBarButton from './components/bar-button'
  import FtSwitch from './components/switch'
  import FtModal from './components/modal'
  export default {
    name: 'application',
    data () {
      return {
        visible: false
      }
    },
    methods: {
      close () {
        console.log(1)
        window.close()
      }
    },
    components: {
      FtIcon,
      FtButton,
      FtBarButton,
      FtSwitch,
      FtModal
    }
  }
</script>

<style lang="scss">
.header {
  width: 100%;
  height: 29px;
  z-index: 100;
  font-size: 0;
  .drag {
    -webkit-app-region: drag;
    display: inline-block;
    height: 100%;
    width: calc(100% - 36px * 3)
  }
}
  /* CSS */
</style>
