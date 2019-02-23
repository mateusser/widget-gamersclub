<template>
  <div id="app">
    <WidgetGC :obj="obj"/>
  </div>
</template>

<script>
import WidgetGC from './components/WidgetGC.vue'

export default {
  name: 'app',
  components: {
    WidgetGC
  },
  data () {
    return {
      obj: {}
    }
  },
  created () {
    fetch('https://api.myjson.com/bins/sqwaq')
      .then((response) => response.json())
      .then((myJson) => {
        this.obj = myJson
      })
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
