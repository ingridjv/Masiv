<template>
  <div class="calificar">    
    <b-form-rating v-model="value"></b-form-rating>

    <p class="mt-2">Value: {{ value }}</p>
  </div>

</template>

<script>
  export default {
    data() {
      return {
        value: null
      }
    }
  }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="less">
   @import '~@/scss/inicio.less'; 
  //@import '../scss/fontawesome.css';  
</style>