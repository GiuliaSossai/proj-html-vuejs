<template>
  <div id="app">
    <Header />
    <Main />
    <Footer />
  </div>
</template>

<script>
import Header from './components/Header.vue';
import Main from './components/Main.vue';
import Footer from './components/Footer.vue';

export default {
  name: 'App',
  components: {
     Header,
     Main,
     Footer      
  },
  data(){
      return {
         
      }
   },
}
</script>

<style lang="scss">
@import '~bootstrap/scss/bootstrap.scss';
@import '~@fortawesome/fontawesome-free/css/all.min.css';

@import './assets/style/vars.scss';
@import './assets/style/generals.scss';
@import './assets/style/mixins.scss';

</style>
