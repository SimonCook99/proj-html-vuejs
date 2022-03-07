<template>
  <div>
    <myHeader :lista="listaHeader"/>

    <myJumbotron />

    <myMain />

    <myFooter :lista="listaFooter"/>
    
  </div>
</template>

<script>
import myHeader from './components/myHeader.vue'
import myJumbotron from './components/myJumbotron.vue'
import myMain from './components/myMain.vue'
import myFooter from './components/myFooter.vue'



export default {
  name: 'App',
  components: {
    myHeader,
    myJumbotron,
    myMain,
    myFooter
  },
  data(){
    return{
      listaHeader: ["Home", "Recipes", "Places", "Blog", "About", "contact"],
      listaFooter: ["Recipes", "Places", "Blog", "About", "contact"]
    }
  }
}
</script>

<style lang="scss">

  @import "./components/SCSS/general.scss";

</style>
