<template>
 <div>
    <Header />
    <Inputs />
 </div>
</template>

<script>

import Header from './components/Header.vue';
import Inputs from './components/Inputs.vue';

export default {
components: {
  Header,
  Inputs
}
}
</script>

<style >  


@import url('https://fonts.googleapis.com/css2?family=Roboto&display=swap');

*{
  margin: 0;
  padding: 0;
  box-sizing: 0;
}
body{
  background: rgb(255,204,181);
background: linear-gradient(90deg, rgba(255,204,181,1) 7%, rgba(175,215,206,1) 51%, rgba(105,169,163,1) 93%);
font-family: 'Roboto', sans-serif;

}



</style>