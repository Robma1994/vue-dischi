<template>
  <div>
    <img :src="vinyl.poster" alt="">
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

</style>
