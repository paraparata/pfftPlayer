<template>
  <div class="container">
    <!-- Game Starter -->
    <div v-if="!done" class="col">
      <button
        type="submit"
        id="tombol"
        @click="updateCount()"
        :style="changeColor()"
      ></button>
    </div>

    <!-- Game over -->
    <div v-if="done" class="col">
      <div v-for="item in result" :key="item.capt" class="sumting">
        <i class="nes-icon" :class="item.trophy"></i>
        <p>{{ item.capt }}</p>
      </div>
      <h1>Gum Uvvur</h1>
    </div>

    <!-- status  -->
    <div class="col">
      <h3>
        You clicked <b>{{ numClicks }}</b> times
      </h3>
      <h4>
        You have <b>{{ secs }}</b> secs left
      </h4>
    </div>

    <div v-if="done" class="col">
      <button type="button" class="nes-btn is-warning" @click="restart()">
        restart
      </button>
    </div>
  </div>
</template>
<script>
export default {
  name: 'Game',
  data() {
    return {
      active: false,
      done: false,
      numClicks: 0,
      secs: 10,
      colors: ['#9bcd77', '#d777b0', '#fed401', '#ff2c3c', '#66c652'],
      color: '',
      width: 200,
      height: 200,
      reward: {
        trophy: '',
        capt: ''
      },
      points: [
        {
          rule: '0',
          trophy: 'coin is-medium',
          capt: 'LOL :v'
        },
        {
          rule: '20',
          trophy: 'coin is-medium',
          capt: 'Yeay, u got a useless coin :('
        },
        {
          rule: '50',
          trophy: 'nes-bulbasaur is-small',
          capt: 'Yeay, u got bulbasaur!! what if..'
        },
        {
          rule: '60',
          trophy: 'nes-charmander is-small',
          capt: 'Maaannn, u got a charming charmander!! hmm..'
        },
        {
          rule: '70',
          trophy: 'nes-squirtle is-small',
          capt: 'Ssss squirtle??? Marvelouss!!!'
        },
        {
          rule: '80',
          trophy: 'nes-kirby is-small',
          capt: 'KIRRBYYYY!!! OMFAntt!!!'
        },
        {
          rule: '100',
          trophy: 'nes-octocat is-small animate',
          capt: 'no doubt, you are a GOD TAPPER!'
        }
      ]
    }
  },

  computed: {
    result: function() {
      return this.points.filter(item => {
        return item.rule < this.numClicks
      })
    }
  },

  mounted() {
    setInterval(() => {
      if (this.active) {
        this.secs--
        if (this.secs == 0) {
          this.active = false
          this.done = true
        }
      }
    }, 1000)
  },

  methods: {
    updateCount() {
      const warna = this.colors[
        Math.round(Math.random() * (this.colors.length - 1))
      ]
      this.numClicks += 1
      this.color = warna

      if (this.active == false) {
        this.secs = 10
        this.numClicks = 1
        this.active = true
      }

      if (this.numClicks % 10 == 0) {
        this.width -= 10
        this.height -= 10
      }
    },
    changeColor() {
      return {
        'background-color': this.color,
        width: this.width + 'px',
        height: this.width + 'px',
        transitionDelay: 500,
        transitionTimingFunction: 'ease-out'
      }
    },
    restart() {
      window.location.reload()
    }
  }
}
</script>
<style scoped>
#tombol {
  border: none;
  color: #fff;
  transition: 0.3s;
  border-radius: 50%;
  background-color: #f2ca27;
}
#tombol:active {
  width: 190px;
  height: 190px;
}
#tombol:focus {
  outline: none;
}
.sumting {
  margin-bottom: 40px;
  font-size: 8pt;
}
</style>
