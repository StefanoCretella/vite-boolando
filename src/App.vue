<template>
  <div id="app">
    <Header />
    <MainContent />
    <Footer />
  </div>
</template>

<script>
import Header from './components/Header.vue'
import MainContent from './components/MainContent.vue'
import Footer from './components/Footer.vue'

export default {
  components: {
    Header,
    MainContent,
    Footer
  }
}
</script>

<style src="./assets/styles/main.scss"></style>
