<template>
  <div class="app-content" @click="getAsyncComponent">
    <component :is="placeholder"></component>
  </div>
</template>
<script>
import LoadComp from './loading-comp'

export default {
  data () {
    return {
      placeholder: LoadComp
    }
  },
  methods: {
    getAsyncComponent () {
      if (this.placeholder === LoadComp) {
        if (!this.ImgContent) {
          this.ImgContent = () => import('./img-content.vue')
        }
        this.ImgContent().then((theComponent) => {
          this.placeholder = theComponent.default
        })
      }
    }
  }
}

</script>

<style lang="scss">
  .app-content {
    position: absolute;
    top: 60px;
    bottom: 60px;
    left: 0;
    right: 0;
    overflow: scroll;
    -webkit-overflow-scrolling: touch;
  }
</style>

