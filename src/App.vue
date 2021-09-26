<template>
  <div id="app">
    <Header :generes="listGenres" />
    
      
    <main class="container-fluid">
       <div class="container d-flex justify-content-center flex-wrap containerBack">
        <Vinyl v-for="(vinyl, index) in listVinyls" 
          :key="index"
          :vinyl = vinyl
        />
      </div>
    </main>
  </div>
</template>

<script>
import axios from 'axios'
import Header from './components/Header.vue'
import Vinyl from './components/Vinyl.vue'

export default {
  name: 'App',
  components: {
    Header,
    Vinyl,
  },
  data() {
    return {
      listVinyls: [],
      listGenres: []
    }
  },
  created() {
      axios
        .get('https://flynn.boolean.careers/exercises/api/array/music')
        .then(result => {
          this.listVinyls = result.data.response
          console.log(this.listVinyls)
          this.listVinyls.forEach((element) => {
            if(!this.listGenres.includes(element.genre)) {
              this.listGenres.push(element.genre)
              console.log(this.listGenres)
            }
          })
        })
  }
}
</script>

<style lang="scss">
//Possiamo non inserire .scss perchè è incluso in lang
@import './style/variables';
@import './style/generals';
.container-fluid {
  background-color: $backgroundMain;
}
.containerBack {
  background-color: $backgroundMain;
  padding: 10px 10px;
  width: 60%;
}

</style>
