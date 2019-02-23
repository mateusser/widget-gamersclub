<template>
  <div class="hello">
    <h1>{{ obj }}</h1>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    obj: Object
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
