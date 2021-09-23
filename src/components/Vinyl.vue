<template>
  <div>
    <div class="containerVynil d-flex flex-column align-items-center">
      <img :src="vinyl.poster" alt="">
      <div class="d-flex flex-column align-items-center justify-content-center text-center">
        <h2 class="titolo">{{vinyl.title}}</h2>
        <h2 class="autore">{{vinyl.author}}</h2>
        <h2 class="anno">{{vinyl.year}}</h2>
      </div>
    </div>
    
  </div>
</template>

<script>
export default {
  name: 'Vinyl',
  props: ['vinyl']
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import '../style/variables';
.containerVynil {
  width: 160px;
  height: 270px;
  background-color: $backgroundContVinyl;
  margin-left: 15px;
    img {
    width: 130px;
    height: 140px;
    padding-top: 20px;
  }
}

.titolo {
  font-size: 16px;
  color: white;
}
.autore, .anno {
  font-size: 12px;
  color: gray;
}

</style>
