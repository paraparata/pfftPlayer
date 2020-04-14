<template>
  <div id="app">
    <Titlebar />
    <router-view />
    <Bottombar />
  </div>
</template>
<script>
import Titlebar from '@/components/Titlebar.vue'
import Bottombar from '@/components/Bottombar.vue'
export default {
  components: { Titlebar, Bottombar }
}
</script>
<style>
@import url('https://fonts.googleapis.com/css2?family=Press+Start+2P&display=swap');

html,
body {
  height: 100%;
  width: 100%;
  margin: 0;
}

#app {
  height: 100%;
  width: 100%;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  font-family: 'Press Start 2P', cursive;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
.container {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}
.col {
  flex: 1;
  margin: 20px;
}

@media (max-width: 600px) {
  .container {
    display: block;
  }
}
</style>
