<template class>
  <div class="header">
   
        <MdFolderOpenIcon  w="60px" h="60px" />
   
   
  </div>
</template>

<script>

import MdFolderOpenIcon from 'vue-ionicons/dist/md-folder-open.vue'



export default {
   name:'HeadeR',
   components: {
    MdFolderOpenIcon
   }

}
</script>




<style scoped>
.header {
    width: 100%;
    height: 70px;
    background: rgb(255,204,181);
background: linear-gradient(90deg, rgba(255,204,181,1) 7%, rgba(175,215,206,1) 51%, rgba(105,169,163,1) 93%);
 display: flex;
 justify-content: center;
 align-items: center;
   
}
.icon {
    width: 30%;
    height: 30%;
}

</style>