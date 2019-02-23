<template>
  <div class="hello">
    <Header :header-info="obj.user" />
  </div>
</template>

<script>
import Header from './Header.vue'

export default {
  props: {
    obj: Object
  },
  components: {
    Header
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
