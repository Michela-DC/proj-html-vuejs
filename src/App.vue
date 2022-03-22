<template>
  <div id="app">
    <HeaderAvada/>
    <main>
      <SectionJumbotron/>
      <SectionTwo/>
      <SectionThree/>
      <SectionFour/>
    </main>
  </div>
</template>

<script>

import HeaderAvada from './components/HeaderAvada.vue'
import SectionJumbotron from './components/SectionJumbotron.vue'
import SectionTwo from './components/SectionTwo.vue'
import SectionThree from './components/SectionThree.vue'
import SectionFour from './components/SectionFour.vue'

export default {
  name: 'App',
  components: {
    HeaderAvada,
    SectionJumbotron,
    SectionTwo,
    SectionThree,
    SectionFour
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
