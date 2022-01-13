<template>
  <div id="app">
    <Header/>
    <Main/>
    <Footer :barber="barberData"/>
  </div>
</template>

<script>
import Header from './components/Header.vue'
import Main from './components/Main.vue'
import Footer from './components/Footer.vue'

export default {
  name: 'App',
  components: {
    Header,
    Main,
    Footer,
  },
  data() {
    return {
      barberData:
        {
          logo: "avadabarbers-logo-x1.png",
          name: "Avada Barbers",
          street: "123 New York Street",
          city: "New York City",
          email: "info@yourwebsite.com",
          phone: "+ 1 (555) 555-1212"
        }
    }
  }
}
</script>

<style lang="scss">
  @import url('https://fonts.googleapis.com/css2?family=Abril+Fatface&display=swap');
  @import url('https://fonts.googleapis.com/css2?family=Lato&display=swap');
  
  * {
    margin: 0;
    padding: 0;
    font-size: 100%;
    box-sizing: border-box;
  }
  .content {
    max-width: 1100px;
    margin: 0 auto;
  }
</style>
