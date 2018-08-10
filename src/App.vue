<template>
  <div id="app">
  	<Left/>
  	<Top/>
    <Chart/>
  </div>
</template>

<script>
import Chart from './components/Chart.vue'
import Top from './components/Top.vue'
import Left from './components/Left.vue'

export default {
  name: 'app',
  components: {
    Chart,
    Top,
    Left
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
