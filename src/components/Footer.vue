<template>
  <div class="footer">
    <a class="item" id="button" href="#0">
      <img src="../assets/assets-front/download.png" style="justify-self: center; align-self: center;"/>
      <span style="justify-self: start; align-self: center;">Download Gamers Club Anti-Cheat</span>
    </a>
    <div class="item" id="online-number"> {{ online }} </div>
    <div class="item" id="onlinewhite"> Jogadores </div>
    <div class="item" id="onlineblue"> Online </div>
    <div class="item" id="cheaters-number"> {{ cheaters }} </div>
    <div class="item" id="cheaterswhite"> Cheaters Banidos </div>
    <div class="item" id="cheatersred"> Nos Últimos 7 Dias </div>
  </div>
</template>

<script>

export default {
  props: {
    online: Number,
    cheaters: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
@import url('https://fonts.googleapis.com/css?family=Teko');

.footer {
  border-radius: 0 0 2px 2px;
  border: 1px solid #333548;
  background-color: #222538;
  display: grid;
  grid-template-columns: 310px auto 50px 75px 50px 130px;
  grid-template-rows: 1fr 1fr;
  grid-template-areas: 
    "button gap online-number onlinewhite cheaters-number cheaterswhite"
    "button gap online-number onlineblue cheaters-number cheatersred";
  grid-column-gap: 10px;   
  grid-row-gap: 1px;   
}

.item {
  justify-self: center;
  align-self: center;
}

#button {
  grid-area: button;
  justify-self: end;
  border-left: 15px;
  width: 295px;
  height: 34px;
  border-radius: 3px;
  background-color: rgba(255, 255, 255, 0.06);
  color: #b6b8c6;
  text-decoration: none;
  font-size: 14px;
  font-weight: 400;
  display: grid;
  grid-template-columns: 40px auto;
  grid-template-rows: 1fr;
}

#online-number {
  grid-area: online-number;
  justify-self: end;
  color: #2c97de;
  font-family: 'Teko', sans-serif;
  font-size: 30px;
  font-weight: 400;
  line-height: 24px;
}

#cheaters-number {
  grid-area: cheaters-number;
  justify-self: end;
  color: #eb2f2f;
  font-family: 'Teko', sans-serif;
  font-size: 30px;
  font-weight: 400;
  line-height: 24px;
}

#onlinewhite {
  grid-area: onlinewhite;
  justify-self: start;
  align-self: end;
  font-size: 12px;
  font-weight: 400;
  line-height: 14px;
}

#onlineblue {
  grid-area: onlineblue;
  justify-self: start;
  align-self: start;
  color: #2c97de;
  font-size: 12px;
  font-weight: 400;
  line-height: 14px;
}

#cheaterswhite {
  grid-area: cheaterswhite;
  justify-self: start;
  align-self: end;
  font-size: 12px;
  font-weight: 400;
  line-height: 14px;
}

#cheatersred {
  grid-area: cheatersred;
  justify-self: start;
  align-self: start;
  color: #eb2f2f;
  font-size: 12px;
  font-weight: 400;
  line-height: 14px;
}
</style>
