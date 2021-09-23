<template>
  <div>
    <div class="container-fluid back-color" >
      <div class="row" style="height: 100px;">
        <div class="col d-flex align-items-center">
          <img class="p-2" style="height: 80px;" src="@/assets/spotify.png" alt="">
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Header'  
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import '../style/variables';
.back-color {
  background-color: $colorHeader;
}

</style>
