<template>
  <div>
    <myHeader :lista="listaHeader"/>

    <myJumbotron />

    
    
  </div>
</template>

<script>
import myHeader from './components/myHeader.vue'
import myJumbotron from './components/myJumbotron.vue'

export default {
  name: 'App',
  components: {
    myHeader,
    myJumbotron
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
