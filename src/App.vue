<template>
  <div>
    <myHeader :lista="listaHeader"/>
    
  </div>
</template>

<script>
import myHeader from './components/myHeader.vue'

export default {
  name: 'App',
  components: {
    myHeader
  },
  data(){
    return{
      listaHeader: ["Home", "Recipes", "Places", "Blog", "About", "contact"]
    }
  }
}
</script>

<style lang="scss">
  *{
    margin: 0;
    padding: 0;
    box-sizing: border-box;
  }
</style>
