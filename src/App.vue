<template>
  <div id="app">
    <HeaderAvada/>
    <main>
      <JumbotronAvada/>
      <FirstBlock/>
    </main>
  </div>
</template>

<script>

import HeaderAvada from './components/HeaderAvada.vue'
import JumbotronAvada from './components/JumbotronAvada.vue'
import FirstBlock from './components/FirstBlock.vue'

export default {
  name: 'App',
  components: {
    HeaderAvada,
    JumbotronAvada,
    FirstBlock,
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
