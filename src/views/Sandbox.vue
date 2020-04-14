<template>
  <div class="sandbox">
    <Game />
  </div>
</template>

<script>
import { Howl } from 'howler'

// @ is an alias to /src
import Game from '@/components/Game.vue'

export default {
  name: 'Sandbox',
  components: {
    Game
  },
  mounted: () => {
    const backsound = new Howl({
      src: ['bgMusic.wav'],
      autoplay: true,
      loop: true,
      volume: 0.5,
      onended: () => console.log('Ended')
    })
    backsound.play()
  }
}
</script>
