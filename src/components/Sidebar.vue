<template>
<div id="container">
    <h2>lista ordini</h2>

    <!-- barra di ricerca  -->
    <div id="search">
            <input type="text" placeholder="n.ordine" v-model="ricerca">
            <i class="bi bi-search"></i>
        </div>
      <div id="container-sidebar">
        
        <ul>
            <li v-for="azienda,i in  aziende" :key="i" :class="i === countervisible ? 'active':''" @click="showall(i),$emit('select-active', countervisible)">
                <div v-if="azienda.ordine.idOrdine.includes(ricerca)" class="contenitore-li">

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
          ricerca:""
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
h2{
    margin-left: 10px;
}
#search{
    background-color: white;
    padding-right:15px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    width: 90%;
    height: 45px;
    border-radius: 30px;
    border: 1px solid gray;
    margin: 5px 0 15px;
    input{
        height: 100%;
        width: 80%;
        border: none;
        padding-left: 15px;
        margin-left: 1px;
        border-radius: 20px;
    }
}
/* Hide scrollbar for Chrome, Safari and Opera */
#container-sidebar::-webkit-scrollbar {
    display: none;
}
/* Hide scrollbar for IE, Edge and Firefox */
#container-sidebar {
-ms-overflow-style: none;  /* IE and Edge */
scrollbar-width: none;  /* Firefox */
}
#container-sidebar{
    background-color: #cacaca;
    width: 100%;
    max-height: 81vh;
    border-radius: 15px;
    padding:10px;
    overflow: scroll;
    box-shadow: 0px 8px 17px 2px rgba(0,0,0,0.14) , 0px 3px 14px 2px rgba(0,0,0,0.12) , 0px 5px 5px -3px rgba(0,0,0,0.2);
    ul{
        .active{
                background-color: rgb(76, 150, 235);
                color: white;
            }
        li{
            list-style: none;
            border-radius: 20px;
            background-color: #ffffff;
            box-shadow: 0px 2px 5px 0px rgba(0,0,0,0.14) , 0px 1px 10px 0px rgba(0,0,0,0.12) , 0px 2px 4px -1px rgba(0,0,0,0.2);
            .contenitore-li{
                padding: 10px;
                margin: 0px 7px 15px;
                display: flex;
                justify-content: space-between;
                align-items: center;
            }
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