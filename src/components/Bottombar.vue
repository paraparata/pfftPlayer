<template>
  <div id="nav">
    <div id="navbar" class="nes-container is-rounded">
      <router-link to="/">Home</router-link> |
      <router-link to="/sandbox">Start</router-link> |
      <router-link to="/about">About</router-link>
    </div>
  </div>
</template>
<script>
export default {
  name: 'Bottombar'
}
</script>
<style scoped>
#nav {
  padding-top: 20px;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
}

#navbar {
  padding: 10px;
}
</style>
