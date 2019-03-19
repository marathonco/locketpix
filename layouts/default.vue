<template>
  <div id="container">
    <Header />
    <div id="wrapper">
      <nuxt />
    </div>
    <Footer />
  </div>
</template>

<script>
import Header from '~/components/layout/Header'
import Footer from '~/components/layout/Footer'

export default {
  components: { Header, Footer },

  methods: {
    restart() {
      this.$router.replace({ path: '/' })
    }
  }
}
</script>

<style lang="scss">
#container {
  align-items: center;
  display: flex;
  min-height: 100vh;
  flex-direction: column;
  position: relative;
}
#wrapper {
  align-items: center;
  background: getColor(background, body);
  border-top: 4px solid getColor(background, light);
  display: flex;
  flex: 1;
  flex-direction: row;
  height: 100%;
  // overflow: hidden;
  // position: relative;
  width: 100%;
  main {
    align-items: center;
    background: getColor(background, body);
    display: flex;
    flex-direction: column;
    justify-content: center;
    padding: 1rem;
    width: 100%;
  }
}
</style>
