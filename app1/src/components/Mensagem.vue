<template>
    <div>
    <input type="text" :value="value" @input="atualizaMensagem"/>
    </div>
</template>
<script>
export default {
    name: 'Mensagem',
    props:['value', 'childData' ],
    data(){
        return {
            mensagem:""
        }
    },
    methods:{
        atualizaMensagem(event){
            this.mensagem = event.target.value; 
            this.childData.mensagem = this.mensagem;
            this.$emit("mensagemMudou", this.mensagem); 
        }
    }
}
</script>
<style scoped>

</style>


