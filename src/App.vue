<template>
  <div id="app">
    <HeaderNavbar/>
    <main>
      <SectionJumbotron/>
      <SectionTwo/>
      <SectionThree/>
      <SectionFour/>
      <SectionFive/>
      <SectionSix/>
    </main>
    <FooterAbout/>
  </div>
</template>

<script>

import HeaderNavbar from './components/HeaderNavbar.vue'
import SectionJumbotron from './components/SectionJumbotron.vue'
import SectionTwo from './components/SectionTwo.vue'
import SectionThree from './components/SectionThree.vue'
import SectionFour from './components/SectionFour.vue'
import SectionFive from './components/SectionFive.vue'
import SectionSix from './components/SectionSix.vue'

import FooterAbout from './components/FooterAbout.vue'


export default {
  name: 'App',
  components: {
    HeaderNavbar,
    SectionJumbotron,
    SectionTwo,
    SectionThree,
    SectionFour,
    SectionFive,
    SectionSix,

    FooterAbout,
  }
}
</script>

<style lang="scss">

@import './assets/scss/common.scss';
@import '@fortawesome/fontawesome-free/css/all.css';

#app {
  font-family: Raleway, sans-serif;
}
</style>
