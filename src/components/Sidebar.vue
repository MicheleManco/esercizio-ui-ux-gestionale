<template>
<div id="container">
    
      <div id="container-sidebar">
          <h2>lista ordini</h2>
      <ul>
        <li v-for="azienda,i in  aziende" :key="i" :class="i === countervisible ? 'active':''" @click="showall(i),$emit('select-active', countervisible)" >
            <div>
                <div class="title-side">{{azienda.ecommerceProvenienza}}</div>
                <div class="n-ordine">n.ordine: <strong>{{azienda.ordine.idOrdine}}</strong> </div>
            </div>
            <select name="stato-ordine" @change="$emit('select',i,$event)" id="selezione">
                <option :value="0">da Spedire</option>
                <option :value="14">spedito</option>
                <option :value="47">transito</option>
                <option :value="100">consegnato</option>
            </select>
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
      //mi serve per dare a i li la classe item se clicco su di essi
      showall(index){
          this.countervisible = index
      }
  }
}
</script>


<style scoped lang="scss">
#container{
    width: 22%;
}
    #container-sidebar{
        background-color: #cacaca;
        width: 100%;
        height: 100%;
        border-radius: 10px;
        padding:8px;
        box-shadow: 0px 8px 17px 2px rgba(0,0,0,0.14) , 0px 3px 14px 2px rgba(0,0,0,0.12) , 0px 5px 5px -3px rgba(0,0,0,0.2);
        h2{
            margin-left: 10px;
        }

        ul{
            width: 100%;
            max-height: 90%;
            overflow: scroll ;
            overflow-x: hidden;
            .active{
                    background-color: rgb(76, 150, 235);
                    color: white;
                }
            li{
                list-style: none;
                border-radius: 10px;
                padding: 10px;
                margin: 12px 7px;
                background-color: #ffffff;
                box-shadow: 0px 2px 5px 0px rgba(0,0,0,0.14) , 0px 1px 10px 0px rgba(0,0,0,0.12) , 0px 2px 4px -1px rgba(0,0,0,0.2);
                display: flex;
                justify-content: space-between;
                align-items: center;
                #selezione{
                    height: 40px;
                    width: 110px;
                    padding-bottom: 3px;
                    padding-left: 4px;
                    border-radius: 10px;
                    border: none;
                    box-shadow: 0px 2px 5px 0px rgba(0,0,0,0.14) , 0px 1px 10px 0px rgba(0,0,0,0.12) , 0px 2px 4px -1px rgba(0,0,0,0.2);
                    background-color: #f0eeee;
                    option{
                        font-size: 20px;
                    }
                }
                .title-side{
                    font-size: 21px;
                }
                
            }
        }
    }


</style>