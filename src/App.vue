<template>
  <div id="app">
    <div id="big-container">
      <Sidebar :aziende = "aziende" @select="selettore"/>
      <MainLayout :aziende = "aziende" :countervisible="countervisible"/>
    </div>
    
  </div>
</template>

<script>
import Sidebar from './components/Sidebar.vue'
import MainLayout from './components/MainLayout.vue'



export default {
  name: 'App',
  components: {
    Sidebar,
    MainLayout
  },
  data(){
    return {
      countervisible : 0,
      aziende: [
        // azienda1 ----------------------------------------------------------------------
        {
          ecommerceProvenienza:"armadio verde",
          ordine: 
              {
              ecommerceProvenienza:"armadio verde",
              data:"10/12/2021",
              valuta:"euro",
              corriere:"ups",
              idOrdine:"78913467",
              pagamento:"carta di credito",
              statoOrdine:"da spedire",
              totSconto:"10%",
              totProdotti:"500€",
              totSpedizione:"80€",
              totIncasso:"400€",
              chiusura:"false",
            
              indirizzo: {
                nome:"gianni",
                cognome:"rossi",
                indirizzo1:"via paola 5",
                indirizzo2:"",
                cap:"36016",
                citta:"thiene",
                nazione:"italia",
                telefono:"3563449862"
              },

              cliente:{
                    nome:"gianni",
                    cognome:"rossi",
                    sesso:"m",
                    email:"giannirossi@mail.com"
                  },

              prodotti:{
                img:"assets/logo.png",
                nome:"penna",
                categoria:"cancelleria",
                quantitaAcquistata:100,
                skulLocation:"cnl-bic-bk-01",
                prezzo:"0.30€",
                quantitaRimanente:1000,
              },

              noteOrdine:{
                operatore:"mario",
                text:"Poche in magazzino, fare rifornimento al prossimo ordine"
              },

              noteCliente:{
                cliente:"armadio verde",
                text:"mi servono entro due settimane, Grazie "
              },
              }
          
        },

        // Azienda 2 ----------------------------------------------------------------------
        {
          ecommerceProvenienza:"fantasia",
          ordine: [
              {
              ecommerceProvenienza:"fantasia",
              data:"10/12/2021",
              valuta:"euro",
              corriere:"ups",
              idOrdine:"17935826",
              pagamento:"carta di credito",
              statoOrdine:"da spedire",
              totSconto:"10%",
              totProdotti:"500€",
              totSpedizione:"80€",
              totIncasso:"400€",
              chiusura:"false",
            
              indirizzo: {
                nome:"gianni",
                cognome:"rossi",
                indirizzo1:"via paola 5",
                indirizzo2:"",
                cap:"36016",
                citta:"thiene",
                nazione:"italia",
                telefono:"3563449862"
              },

              cliente:{
                    nome:"gianni",
                    cognome:"rossi",
                    sesso:"m",
                    email:"giannirossi@mail.com"
                  },

              prodotti:{
                img:"assets/logo.png",
                nome:"penna",
                categoria:"cancelleria",
                quantitaAcquistata:100,
                skulLocation:"cnl-bic-bk-01",
                prezzo:"0.30€",
                quantitaRimanente:1000,
              },

              noteOrdine:{
                operatore:"mario",
                text:"Poche in magazzino, fare rifornimento al prossimo ordine"
              },

              noteCliente:{
                cliente:"armadio verde",
                text:"mi servono entro due settimane, Grazie "
              },
              }
          ]
        },

        // Azienda 3 ----------------------------------------------------------------------
        {
          ecommerceProvenienza:"armadio verde",
          ordine: [
              {
              ecommerceProvenienza:"armadio verde",
              data:"10/12/2021",
              valuta:"euro",
              corriere:"ups",
              idOrdine:"10000021",
              pagamento:"carta di credito",
              statoOrdine:"da spedire",
              totSconto:"10%",
              totProdotti:"500€",
              totSpedizione:"80€",
              totIncasso:"400€",
              chiusura:"false",
            
              indirizzo: {
                nome:"gianni",
                cognome:"rossi",
                indirizzo1:"via paola 5",
                indirizzo2:"",
                cap:"36016",
                citta:"thiene",
                nazione:"italia",
                telefono:"3563449862"
              },

              cliente:{
                    nome:"gianni",
                    cognome:"rossi",
                    sesso:"m",
                    email:"giannirossi@mail.com"
                  },

              prodotti:{
                img:"assets/logo.png",
                nome:"penna",
                categoria:"cancelleria",
                quantitaAcquistata:100,
                skulLocation:"cnl-bic-bk-01",
                prezzo:"0.30€",
                quantitaRimanente:1000,
              },

              noteOrdine:{
                operatore:"mario",
                text:"Poche in magazzino, fare rifornimento al prossimo ordine"
              },

              noteCliente:{
                cliente:"armadio verde",
                text:"mi servono entro due settimane, Grazie "
              },
              }
          ]
        },

        // azienda4 ----------------------------------------------------------------------
        {
          ecommerceProvenienza:"amazon",
          ordine: [
              {
                ecommerceProvenienza:"amazon",
                data:"10/12/2021",
                valuta:"euro",
                corriere:"ups",
                idOrdine:"19743467",
                pagamento:"carta di credito",
                statoOrdine:"da spedire",
                totSconto:"10%",
                totProdotti:"500€",
                totSpedizione:"80€",
                totIncasso:"400€",
                chiusura:"false",

              indirizzo: [{
                nome:"gianni",
                cognome:"rossi",
                indirizzo1:"via paola 5",
                indirizzo2:"",
                cap:"36016",
                citta:"thiene",
                nazione:"italia",
                telefono:"3563449862"
              }],

              cliente:[{
                    nome:"gianni",
                    cognome:"rossi",
                    sesso:"m",
                    email:"giannirossi@mail.com"
                  }],

              prodotti:[{
                img:"assets/logo.png",
                nome:"penna",
                categoria:"cancelleria",
                quantitaAcquistata:100,
                skulLocation:"cnl-bic-bk-01",
                prezzo:"0.30€",
                quantitaRimanente:1000,
              }],

              noteOrdine:[{
                operatore:"mario",
                text:"Poche in magazzino, fare rifornimento al prossimo ordine"
              }],

              noteCliente:[{
                cliente:"amazon",
                text:"mi servono entro domani"
              }],
              }
          ]
        }
      ]
    }
  },
  methods:{
    selettore(count){
      this.countervisible = count
      console.log(this.countervisible);
    }
  }
}

</script>

<style lang="scss">
*{
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}
body{
  background-color: rgb(216, 215, 215);
  #big-container{
    height: 100vh;
    padding: 20px;
    display: flex;
    justify-content: space-between;
  }
}

</style>
