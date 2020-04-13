<template>
  <div id="nav">
    <div id="navbar" class="nes-container is-rounded">
      <code class="pfft">pfft</code>Player
    </div>
  </div>
</template>
<script>
export default {
  name: 'Titlebar'
}
</script>
<style scoped>
#nav {
  margin-bottom: 20px;
  padding-top: 20px;
  display: flex;
  justify-content: center;
  font-weight: bold;
  color: #2c3e50;
}

.pfft {
  font-weight: lighter;
  color: #42b983;
}

#navbar {
  padding: 10px;
  width: fit-content;
}
</style>
