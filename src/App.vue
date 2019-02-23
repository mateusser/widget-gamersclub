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
        console.log(JSON.parse(JSON.stringify(myJson)))
      })
  }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css?family=Poppins');

#app {
  font-family: 'Poppins', sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: left;
  color: #FFFFFF;
  margin-top: 60px;
}
</style>
