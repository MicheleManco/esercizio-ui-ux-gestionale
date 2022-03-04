<template>
<div id="container">
    
      <div id="container-sidebar">
          <h2>lista ordini</h2>
      <ul>
        <li v-for="azienda,i in  aziende" :key="i" :class="i === countervisible ? 'active':''" @click="showall(i),$emit('select', countervisible)" >
            <div>
                <div class="title-side">{{azienda.ecommerceProvenienza}}</div>
                <div class="n-ordine"> n.ordine:{{azienda.ordine.idOrdine}} </div>
            </div>
        </li>
      </ul>

  </div>    
</div>

</template>

<script>
export default {
  name: 'Sidebar',
  data(){
      return{
          countervisible:0,
      }
  },
  props:{
      aziende:Array,
  },
  methods:{
      //mi serve per dare a i li la classe item se clicco sudi essi
      showall(index){
          this.countervisible = index
      }
  }
}
</script>


<style scoped lang="scss">
#container{
    width: 20%;
}
    #container-sidebar{
        background-color: rgb(200, 228, 231);
        width: 100%;
        height: 100%;
        border-radius: 10px;
        padding:8px;
        box-shadow: 0px 8px 17px 2px rgba(0,0,0,0.14) , 0px 3px 14px 2px rgba(0,0,0,0.12) , 0px 5px 5px -3px rgba(0,0,0,0.2);
        

        ul{
            width: 100%;
            max-height: 90%;
            overflow: scroll ;
            overflow-x: hidden;
            .active{
                    background-color: rgb(28, 191, 255);
                }
            li{
                list-style: none;
                border-radius: 10px;
                padding: 10px;
                margin: 12px 7px;
                background-color: rgb(245, 249, 250);
                box-shadow: 0px 2px 5px 0px rgba(0,0,0,0.14) , 0px 1px 10px 0px rgba(0,0,0,0.12) , 0px 2px 4px -1px rgba(0,0,0,0.2);
                
                .title-side{
                    font-size: 21px;
                }
                .n-ordine{
                    color: gray;
                }
            }
        }
    }


</style>