<template>
<div id="container">
          <div>{{aziende[countervisible].ecommerceProvenienza}}</div>
          <div>{{aziende[countervisible].ordine.prodotti.nome}}</div>
</div>

</template>

<script>
export default {
  name: 'MainLayout',
  data(){
      return{

      }
  },
  props:{
      aziende:Array,
      countervisible:Number
  }
}
</script>


<style scoped lang="scss">
#container{
  width: 79%;
  background-color: yellow;
  background-color: rgb(200, 228, 231);
  height: 100%;
  border-radius: 10px;
  padding:8px;
  box-shadow: 0px 8px 17px 2px rgba(0,0,0,0.14) , 0px 3px 14px 2px rgba(0,0,0,0.12) , 0px 5px 5px -3px rgba(0,0,0,0.2);
}
</style>