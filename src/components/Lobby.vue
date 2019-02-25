<template>
  <div class="lobby">
    <div class="item" id="title">
      <img src="../assets/assets-front/Lobby.svg" height="25" />
      <span> {{ info.title }} </span>
    </div>
    <div class="item display" id="total">
      <div />
      <span class="number" style="color: #ddbc39;"> {{ info.matches }} </span>
      <span class="main"> PARTIDAS </span>
    </div>
    <div class="item display" id="win">
      <div />
      <span class="number" style="color: #92aa00;"> {{ info.win }} </span>
      <span class="main"> VITÓRIAS </span>
    </div>
    <div class="item display" id="loss">
      <div />
      <span class="number" style="color: #fc3537;"> {{ info.lose }} </span>
      <span class="main"> DERROTAS </span>
    </div>
    <a class="item" id="button" :href="info.cta.link">
      <span>
        {{ info.cta.title }}
      </span>
    </a>
  </div>
</template>

<script>
export default {
  props: {
    info: Object
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
@import url('https://fonts.googleapis.com/css?family=Teko');

.lobby {
  border-radius: 0 0 2px 2px;
  border: 1px solid #333548;
  background-color: #222538;
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
  grid-template-rows: 50px auto 70px;
  grid-template-areas: 
    "title title title"
    "total win loss"
    "button button button";
  color: #ffffff;
  font-family: 'Teko', sans-serif;
}

.item {
  justify-self: center;
  align-self: center;
}

.main {
  font-size: 17px;
  font-weight: 400;
  text-transform: uppercase;
  text-align: center;
}

.number {
  font-size: 37px;
  font-weight: 400;
  line-height: 32px;
  text-align: center;
}

.display {
  width: 93px;
  height: 103px;
  border-radius: 2px;
  background-image: linear-gradient(180deg, rgba(238, 238, 238, 0.1) 0%, rgba(255, 255, 255, 0) 100%);
  display: grid;
  grid-template-rows: 11px auto 50px;  
  grid-template-columns: 1fr;  
  grid-column-gap: 10px;
}

#title {
  grid-area: title;
  justify-self: start;
  font-size: 20px;
  font-weight: 400;
  text-transform: uppercase;
  display: grid;
  grid-template-columns: 50px auto;
  justify-items: center;
}

#total {
  grid-area: total;
}

#win {
  grid-area: win;
}

#loss {
  grid-area: loss;
}

#button {
  grid-area: button;
  justify-self: center;
  align-self: center;
  border-left: 15px;
  width: 284px;
  height: 40px;
  border-radius: 2px;
  border: 1px solid rgba(255, 255, 255, 0.1);
  background-color: #ddbc39;
  background-image: linear-gradient(180deg, rgba(255, 255, 255, 0.25) 0%, rgba(255, 255, 255, 0) 100%);
  box-shadow: 0 6px 6px -3px rgba(0, 0, 0, 0.25), inset 0 1px 0 rgba(255, 255, 255, 0.25);
  color: #ffffff;
  font-size: 20px;
  font-weight: 400;
  line-height: 24px;
  text-transform: uppercase;
  text-decoration: none;
  display: grid;
  justify-items: center;
  align-items: center;
}
</style>
