<!-- Padre -->
<template>
  <div>
    <div class="container d-flex justify-content-center flex-wrap containerBack">
      <Vinyl v-for="(vinyl, index) in listVinyls" 
        :key="index"
        :vinyl = vinyl
      />
    </div>
     
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
@import '../style/variables';
.containerBack {
  background-color: $backgroundMain;
  padding: 10px 10px;
  height: 621px;
  width: 60%;
}

</style>
