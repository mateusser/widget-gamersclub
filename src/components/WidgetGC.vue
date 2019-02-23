<template>
  <div class="widget">
    <Header class="header" :header-info="obj.user" />
    <div class="fun" />
    <div class="lobby" />
    <div class="ranked" />
    <Footer class="footer" :online="obj.online" :cheaters="obj.latest_banned" />
  </div>
</template>

<script>
import Header from './Header.vue'
import Footer from './Footer.vue'

export default {
  props: {
    obj: Object
  },
  components: {
    Header,
    Footer
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.widget {
  display: grid;
  grid-template-columns: 546px auto 306px;
  grid-template-rows: 93px auto 53px;
  grid-template-areas: 
    "header header header"
    "fun lobby ranked"
    "footer footer footer";
  grid-column-gap: 5px;   
  width: 1172px;
  height: 370px;
  box-shadow: 0 8px 16px -4px rgba(0, 0, 0, 0.5);
  border-radius: 2px;
  border: 1px solid #333548;
  background-color: #27293c;
}

.header{
  grid-area: header;
}

.footer{
  grid-area: footer;
}

.fun{
  grid-area: fun;
}

.lobby{
  grid-area: lobby;
}

.ranked{
  grid-area: ranked;
}
</style>
