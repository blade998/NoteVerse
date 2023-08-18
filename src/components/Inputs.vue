<template>
    
  <div class="container-inputs">
    <input v-model="nome" type="text" placeholder="Escreva Seu nome">
    <input v-model="anotacao" type="text" placeholder="Escreva Sua anotação">
    <button @click="mostrardados">Cadastrar Anotação</button>
  <div class="ta"  v-for="(lembretes, index) in lembretes" :key="index">
    <Anotacoes @excluir= 'apagarlembrete(index)' :nome="lembretes.nome" :anotacao="lembretes.anotacao" />
</div> 
   
    
   

   
   
  </div>
 
  

</template>

<script>

import Anotacoes from './Anotacoes.vue';




export default {
   name:'InputS',
   components:{
    Anotacoes
   },
   data() {
    return {
        nome:'',
        anotacao:'',
        lembretes: []
    }
    
    
    
   },
   methods: {
     mostrardados(){
      this.lembretes.push({
        nome: this.nome,
        anotacao: this.anotacao
      });
      this.nome = '';
      this.anotacao = '';


        
     },
   
     apagarlembrete(index) {
      this.lembretes.splice(index, 1);
      console.log(this.lembretes);
     }
   }


   
   
}







</script>

<style scoped>


.container-inputs{
    width: 100%;
    height: auto;
   display: flex;
    gap: 40px;
    flex-direction: column;
    justify-content: center;
    align-items: center;

}
input{
height:60px;
width:50% ;
border-radius: 30px;
    border: 2px solid black;
}
button{
    width: 179px;
    height: 60px;
    border-radius: 30px;
    border: 2px solid black;
}
button:hover {
  background-color: white ;
}

button:active {
  transform: scale(0.95);
  background-color: #ccc;
}

.ta {
    width: 100%;
    display: flex;
    flex-direction: center;
    justify-content: center;
    align-items: center;
}
</style>