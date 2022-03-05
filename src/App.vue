<template>
  <div>
    <myHeader :lista="listaHeader"/>

    <myJumbotron />

    <myMain />
    
  </div>
</template>

<script>
import myHeader from './components/myHeader.vue'
import myJumbotron from './components/myJumbotron.vue'
import myMain from './components/myMain.vue'


export default {
  name: 'App',
  components: {
    myHeader,
    myJumbotron,
    myMain
  },
  data(){
    return{
      listaHeader: ["Home", "Recipes", "Places", "Blog", "About", "contact"]
    }
  }
}
</script>

<style lang="scss">

  @import "./components/SCSS/general.scss";

</style>
