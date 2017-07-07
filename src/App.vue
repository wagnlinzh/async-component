<template>
  <div id="app">
    <app-header></app-header>
    <app-content></app-content>
    <app-footer></app-footer>
  </div>
</template>

<script>
import AppHeader from './components/app-header'
import AppContent from './components/app-content'
import AppFooter from './components/app-footer'
export default {
  name: 'app',
  components: {
    AppHeader,
    AppContent,
    AppFooter
  }
}
</script>

<style>
  * {
    padding: 0;
    margin: 0;
  }
  
  *::after {
    box-sizing: border-box;
  }
  
  #app {
    font-family: 'Avenir', Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
  }
  
  h2 {
    border-bottom: 1px solid #eee;
  }
</style>
