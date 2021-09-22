<!-- Padre -->
<template>
  <div>
    <Vinyl v-for="(vinyl, index) in listVinyls" 
      :key="index"
      :vinyl = vinyl
    /> 

  </div>
</template>

<script>
import axios from 'axios'
import Vinyl from './Vinyl.vue'
export default {
  name: 'Vinyls',
  components: {
    Vinyl
  },
  data() {
    return {
      listVinyls: []
    }
  },
  mounted() {
      axios
        .get('https://flynn.boolean.careers/exercises/api/array/music')
        .then(result => {
          this.listVinyls = result.data.response
          console.log(this.listVinyls)
        })
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">

</style>
