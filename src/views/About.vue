<template>
  <div class="about">
    <div class="aboutLagi">
      <h1>This is an about page,</h1>
      <div class="container">
        <div class="col nes-container with-title is-centered">
          <p class="title">Hey there!</p>
          <p>Syari roti, roti syari roti.</p>
        </div>
      </div>
    </div>
    <div class="credit">
      <p class="tituru">made with wuv by <em class="ijo">paraparata</em></p>
      <p>
        anyway if u want to contribute just fork this on my
        <a
          href="https://github.com/paraparata/pfftPlayer"
          target="_"
          class="ijo"
          >Github <i class="nes-icon github is-small"></i>
        </a>
        , it's open source.
      </p>
    </div>
  </div>
</template>
<style scoped>
.about {
  height: 100%;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}
.aboutLagi {
  height: 80%;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}
.credit {
  padding: 0 16px;
  font-size: 6pt;
}
.tituru {
  margin-bottom: 10px;
  font-size: 8pt;
}
.ijo {
  color: #42b983;
  text-decoration: none;
}
</style>
