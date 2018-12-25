<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <HelloWorld msg="Welcome" >
      <template slot-scope="{ childdata }">
        <mensagem v-model="mensagem" :childData="childdata" @mensagemMudou="mensagem=$event">
        </mensagem>
        <br/>Objeto 'childdata' escopado pelo HelloWorld.vue e repassado a Mensagem.vue via propertie:{{childdata}}
      </template> 
    </HelloWorld>
    <br/>Mensagem em app.vue passada para Mensagem.vue (valor do input): {{mensagem}}
    
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import Mensagem from './components/Mensagem.vue'

export default {
  name: 'app',
  components: {
    HelloWorld, Mensagem
  },
  data: function(){
    return {mensagem:'moacyr'}
  },
  created(){
   // console.log("criou o app");
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
