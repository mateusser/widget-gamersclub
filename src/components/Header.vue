<template>
  <div class="header">
    <div class="item" id="avatar">
      <img src="../assets/assets-front/avatar.png" height="45" width="45" />
    </div>
    <div class="item" id="name">{{ headerInfo.name }} </div>
    <div class="item" id="id">
      GC ID: {{ headerInfo.id }}
    </div>
    <div class="item" id="expertise">
      expertise: {{ headerInfo.expertise }}
    </div>
    <div class="item" id="medal">
      <img
        :src="headerInfo.featured_medal.image"
        width="45"
      />
    </div>
    <div class="item" id="position">
      <img
        :src="headerInfo.game_position.image"
        :alt="headerInfo.game_position.title"
        width="45"
      />
    </div>
    <div class="item" id="patent">
      <img
        :src="headerInfo.patent"
        width="45"
      />
    </div>
    <div class="item" id="level-circle" />
    <div class="item" id="level-value">{{ headerInfo.level }}</div>
    <div class="item" id="premium-background" />
    <div class="item" id="premium-image">
      <img src="../assets/assets-front/premium-ii-medal.png" height="54" width="47" />
    </div>

  </div>
</template>

<script>

export default {
  props: {
    headerInfo: Object
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.header {
  background-image: url('../assets/assets-front/header-background.png');
  box-shadow: 0 8px 16px -4px rgba(0, 0, 0, 0.3);
  border-radius: 2px 2px 0 0;
  background-color: #272940;
  display: grid;
  grid-template-columns: 70px auto 515px 60px 60px 60px 60px 83px;
  grid-template-rows: 50% 50%;
  grid-template-areas: 
    "avatar name expertise medal position patent level premium"
    "avatar id expertise medal position patent level premium";
  grid-column-gap: 5px;   
}

.item {
  justify-self: center;
  align-self: center;
}

#avatar {
  grid-area: avatar;
}

#name {
  grid-area: name;
  justify-self: start;
  align-self: end;
  font-size: 16px;
  font-weight: 500;
  line-height: 24px;
  white-space: nowrap; 
  overflow: hidden;
  text-overflow: ellipsis;
}

#id {
  grid-area: id;
  justify-self: start;
  align-self: start;
  color: #7c7da3;
  font-size: 12px;
  font-weight: 500;
  line-height: 16px;
}

#expertise {
  grid-area: expertise;
}

#position {
  grid-area: position;
}

#patent {
  grid-area: patent;
}

#medal {
  grid-area: medal;
}

#level-circle {
  grid-area: level;
  border: 2px solid rgba(255, 255, 255, 0.2);
  border-radius: 23px;
  width: 45px;
  height: 45px;
}
#level-value {
  grid-area: level;
  font-size: 19px;
  font-weight: 500;
  line-height: 16.54px;
  text-align: center;
}

#premium-background {
  grid-area: premium;
  width: 83px;
  height: 93px;
  background-image: radial-gradient(circle at center, #19f3ff 0%, #3883db 100%);
}

#premium-image {
  grid-area: premium;
}
</style>
