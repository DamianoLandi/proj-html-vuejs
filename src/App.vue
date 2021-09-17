<template>
  <div id="app">
    <Header/>
    <Main/>
    <Footer/>
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
    Footer
  }
}
</script>

<style lang="scss">

body{
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
}

/* Utils */

.container{
  width: 1200px;
  margin: auto;
}

.container-small{
  width: 800px;
  margin: auto;
}

.container-xs{
  width: 500px;
  margin: auto;
}

ul{
    list-style-type: none;
    padding: 0;
}

.text-gray{
  color: #62676c;
}

.col-8{
    flex-basis: calc(100% / 3 * 2);
}

.col-4{
    flex-basis: calc(100% / 3);
}

.col-3{
    flex-basis: calc(100% / 4);
}

</style>
