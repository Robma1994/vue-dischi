<template>
  <div class="d-flex">
    <div class="ContHeader" >
      <div class="row" style="height: 100px;">
        <div class="col d-flex align-items-center">
          <img class="p-2" style="height: 80px;" src="@/assets/spotify.png" alt="">
        </div>
      </div>
    </div>
    <div class="contHeaderOption">
      <form>
        <select class="containerSelect"> 
          <option v-for="(geners,index) in generes" :key="index" value="">
            {{geners}} 
          </option>
        </select>
      </form>
      
    </div>
    
  </div>
</template>

<script>

export default {
  name: 'Header',
  props: ['generes'],
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import '../style/variables';
.ContHeader {
  background-color: $colorHeader;
  width: 50%;
}
.contHeaderOption {
  background-color: $colorHeader;
  width: 50%; 
  display: flex;
  align-items: center;
  justify-content: end;
  padding-right: 140px;

    .containerSelect {
    height: 40px;
    width: 180px;
  }
}

</style>
