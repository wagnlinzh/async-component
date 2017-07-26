<template>
  <div class="app-content" >
    <async-com></async-com>
  </div>
</template>
<script>
import LoadComp from './loading-comp'
import errCom from './error-comp'

const asyncCom = () => ({
  component: new Promise((resolve, reject) => {
    setTimeout(() => {
      resolve(import('./asyncCom.vue'))
    }, 2000)
  }),
  loading: LoadComp,
  error: errCom,
  delay: 200,
  timeout: 1000
})

export default {
  data () {
    return {
      placeholder: LoadComp
    }
  },
  components: {
    asyncCom
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

