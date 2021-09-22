<template>
  <div id="app" class="text-center">
    <Header/>
    <main>
      <Vinyls /> <!-- Padre -->
    </main>
    
  </div>
</template>

<script>
import Header from './components/Header.vue'
import Vinyls from './components/Vinyls.vue'

export default {
  name: 'App',
  components: {
    Header,
    Vinyls
  }
}
</script>

<style lang="scss">
//Possiamo non inserire .scss perchè è incluso in lang
@import './style/generals';
</style>
