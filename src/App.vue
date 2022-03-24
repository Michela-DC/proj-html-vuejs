<template>
  <div id="app">
    <HeaderNavbar/>
    <main>
      <SectionJumbotron/>
      <SectionQuestion/>
      <SectionSpecialists/>
      <SectionNumbers/>
      <SectionExplore/>
      <SectionValues/>
      <SectionOwners/>
      <SectionNews/>
      <SectionPartners/>
      <SectionInspiring/>
    </main>
    <FooterAbout/>
  </div>
</template>

<script>

import HeaderNavbar from './components/HeaderNavbar.vue'
import SectionJumbotron from './components/SectionJumbotron.vue'
import SectionQuestion from './components/SectionQuestion.vue'
import SectionSpecialists from './components/SectionSpecialists.vue'
import SectionNumbers from './components/SectionNumbers.vue'
import SectionExplore from './components/SectionExplore.vue'
import SectionValues from './components/SectionValues.vue'
import SectionOwners from './components/SectionOwners.vue'
import SectionNews from './components/SectionNews.vue'
import SectionPartners from './components/SectionPartners.vue'
import SectionInspiring from './components/SectionInspiring.vue'
import FooterAbout from './components/FooterAbout.vue'

export default {
  name: 'App',
  components: {
    HeaderNavbar,
    SectionJumbotron,
    SectionQuestion,
    SectionSpecialists,
    SectionNumbers,
    SectionExplore,
    SectionValues,
    SectionOwners,
    SectionNews,
    SectionPartners,
    SectionInspiring,
    FooterAbout
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
