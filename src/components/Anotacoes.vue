<template>
  <div class="container-card">
    <header class="header-card">
    <div class="name">{{ nome }}</div>
    <div class="icon">
        <button  @click="apagar" class="apagar">
      <MdCloseIcon w="20px" h="30px"/>
    </button>
    </div>
    </header>
    <div class="header-anotacao">Anotação:</div>
    <div class="text">{{ anotacao }}</div>
  </div>
</template>

<script>



import MdCloseIcon from 'vue-ionicons/dist/md-close.vue'




export default {
   name:'AnotacoeS' ,
   components:{
    MdCloseIcon
   },
   props: ['nome', 'anotacao'],
   methods: {
    apagar() {
        console.log('executou')
        this.$emit('excluir')
       
    }
   }
}
</script>

<style>
.container-card{
    
    color: black;
    width: 50%;
    height: 350px;
    background-color: #69a9a3;
    border-radius: 21px;
    box-shadow: 5px -3px 13px 1px #000;
    padding: 5px;

}
.header-card {
    display: flex;
    justify-content: space-between;
    font-size: larger;
}
.icon{
    padding: 4px;
   
}
.name{
    padding: 4px;
}
.header-anotacao{
    font-size: larger;
}
.text{
    margin-top: 3px;
}

@media(max-width:700px){
    .container-card{
    width: 90%;
    height: 400px;
  
    }
}
.apagar{

 
border-radius:50%;
  width: 60px;
  height: 60px;
  font-size: inherit;
  color: inherit;
  cursor: pointer;

}



</style>