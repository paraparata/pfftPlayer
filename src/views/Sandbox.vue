<template>
  <div class="sandbox">
    <Game />
  </div>
</template>

<script>
// @ is an alias to /src
import Game from '@/components/Game.vue'

export default {
  name: 'Sandbox',
  components: {
    Game
  }
}
</script>
