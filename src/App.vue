<template>
  <div id="app">
    <HeaderAvada/>
    <main>
      <JumbotronAvada/>
    </main>
  </div>
</template>

<script>

import HeaderAvada from './components/HeaderAvada.vue'
import JumbotronAvada from './components/JumbotronAvada.vue'

export default {
  name: 'App',
  components: {
    HeaderAvada,
    JumbotronAvada,
  }
}
</script>

<style lang="scss">

@import './assets/scss/common.scss';

#app {
  font-family: Raleway, sans-serif;
}
</style>
