<template>
  <div class="hello">
      {{msg}}, <slot :childdata="dataHello"></slot>
      <br/>Objeto 'dataHello' em Helloworld.vue exposto pelo slot:{{dataHello}}
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  data:function(){
    return {
      dataHello:{nome:'', mensagem:'mensagem inicial'}
    }
  },
  created: function(){
//    this.$on('fiomudou', function (event){
//      console.log(event);
//    });
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
