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
        // azienda1 -----------------------------------------------------------------------
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
              totSconto: 10,
              totProdotti:500,
              totSpedizione:80,
              totIncasso: 410,
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

              prodotti:[
                {
                img:"assets/penna.png",
                nome:"Penna",
                categoria:"cancelleria",
                quantitaAcquistata:100,
                skulLocation:"cnl-bic-bk-01",
                prezzo:0.30,
                quantitaRimanente:1000,
              },
              {
                img:"assets/penna.png",
                nome:"Penna",
                categoria:"cancelleria",
                quantitaAcquistata:100,
                skulLocation:"cnl-bic-bk-01",
                prezzo:0.30,
                quantitaRimanente:1000,
              },
              {
                img:"assets/penna.png",
                nome:"Penna",
                categoria:"cancelleria",
                quantitaAcquistata:100,
                skulLocation:"cnl-bic-bk-01",
                prezzo:0.30,
                quantitaRimanente:1000,
              },
              {
                img:"assets/penna.png",
                nome:"Penna",
                categoria:"cancelleria",
                quantitaAcquistata:100,
                skulLocation:"cnl-bic-bk-01",
                prezzo:0.30,
                quantitaRimanente:1000,
              },
              {
                img:"assets/penna.png",
                nome:"Penna",
                categoria:"cancelleria",
                quantitaAcquistata:100,
                skulLocation:"cnl-bic-bk-01",
                prezzo:0.30,
                quantitaRimanente:1000,
              },
              

              {
                img:"assets/matita.png",
                nome:"Matita",
                categoria:"cancelleria",
                quantitaAcquistata:50,
                skulLocation:"cnl-mat-rd-12",
                prezzo:0.30,
                quantitaRimanente:800,
              }
              ],

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
          ordine: 
              {
              ecommerceProvenienza:"fantasia",
              data:"10/12/2021",
              valuta:"euro",
              corriere:"ups",
              idOrdine:"17935826",
              pagamento:"carta di credito",
              statoOrdine:"da spedire",
              totSconto:10,
              totProdotti:500,
              totSpedizione:80,
              totIncasso:400,
              chiusura:"false",
            
              indirizzo: {
                nome:"Franca",
                cognome:"Verdi",
                indirizzo1:"via san gaetano 5",
                indirizzo2:"",
                cap:"50121",
                citta:"Firenze",
                nazione:"italia",
                telefono:"6591778349"
              },

              cliente:{
                    nome:"Franca",
                    cognome:"Verdi",
                    sesso:"f",
                    email:"Francaverdi@mail.com"
                  },

              prodotti:[
                {
                img:"assets/logo.png",
                nome:"aspirapolvere",
                categoria:"casa",
                quantitaAcquistata:100,
                skulLocation:"csa-dsy-wh-18",
                prezzo:0.30,
                quantitaRimanente:1000,
              },
              {
                img:"assets/logo.png",
                nome:"lavatrice",
                categoria:"casa",
                quantitaAcquistata:50,
                skulLocation:"csa-art-wh-30",
                prezzo:0.30,
                quantitaRimanente:800,
              }
              ],

              noteOrdine:{
                operatore:"mario",
                text:"Poche in magazzino, fare rifornimento al prossimo ordine"
              },

              noteCliente:{
                cliente:"fantasia",
                text:"sdognbsigujdnghosignhosgnosg nsoldikgjnowesringsoikjfgsiokedigukhnasogikjusnedog idkjgnfvmaoikgfjnosuijknhgisegujnhsoeguij jhnsoigernhsiogkshjoregujishnogiujs hnogishngirujdngsiogsneodigf jsoiguseordgishngioshn"
              },
              }
          
        },
        // Azienda 3 ----------------------------------------------------------------------
        {
          ecommerceProvenienza:"armadio verde",
          ordine: 
              {
              ecommerceProvenienza:"armadio verde",
              data:"10/12/2021",
              valuta:"euro",
              corriere:"ups",
              idOrdine:"10000021",
              pagamento:"carta di credito",
              statoOrdine:"da spedire",
              totSconto:10,
              totProdotti:500,
              totSpedizione:80,
              totIncasso:400,
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

              prodotti:[
                {
                img:"assets/logo.png",
                nome:"felpa",
                categoria:"abbigliamento",
                quantitaAcquistata:100,
                skulLocation:"abb-avr-ylw-11",
                prezzo:0.30,
                quantitaRimanente:1000,
              },
              ],

              noteOrdine:{
                operatore:"mario",
                text:"Poche in magazzino, fare rifornimento al prossimo ordine"
              },

              noteCliente:{
                cliente:"armadio verde",
                text:"mi serve che siano imballate con attenzione perchè sono estremamente fragili e potrebbe capitare che si rompano"
              },
              }
          
        },
        // azienda4 -----------------------------------------------------------------------
        {
          ecommerceProvenienza:"amazon",
          ordine: 
              {
                ecommerceProvenienza:"amazon",
                data:"10/12/2021",
                valuta:"euro",
                corriere:"ups",
                idOrdine:"19743467",
                pagamento:"carta di credito",
                statoOrdine:"da spedire",
                totSconto:10,
                totProdotti:500,
                totSpedizione:80,
                totIncasso:400,
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

              prodotti:[
                {
                img:"assets/logo.png",
                nome:"penna",
                categoria:"cancelleria",
                quantitaAcquistata:100,
                skulLocation:"cnl-bic-bk-01",
                prezzo:0.30,
                quantitaRimanente:1000,
              },
              {
                img:"assets/logo.png",
                nome:"matita",
                categoria:"cancelleria",
                quantitaAcquistata:50,
                skulLocation:"cnl-bic-bk-01",
                prezzo:0.30,
                quantitaRimanente:800,
              }
              ],

              noteOrdine:{
                operatore:"mario",
                text:"Poche in magazzino, fare rifornimento al prossimo ordine"
              },

              noteCliente:{
                cliente:"amazon",
                text:"mi servono entro domani"
              },
              }
          
        },
        // aziende di test ----------------------------------------------------------------
        {
          ecommerceProvenienza:"fantasia",
          ordine: 
              {
              ecommerceProvenienza:"fantasia",
              data:"10/12/2021",
              valuta:"euro",
              corriere:"ups",
              idOrdine:"17935826",
              pagamento:"carta di credito",
              statoOrdine:"da spedire",
              totSconto:10,
              totProdotti:500,
              totSpedizione:80,
              totIncasso:400,
              chiusura:"false",
            
              indirizzo: {
                nome:"Franca",
                cognome:"Verdi",
                indirizzo1:"via san gaetano 5",
                indirizzo2:"",
                cap:"50121",
                citta:"Firenze",
                nazione:"italia",
                telefono:"6591778349"
              },

              cliente:{
                    nome:"Franca",
                    cognome:"Verdi",
                    sesso:"f",
                    email:"Francaverdi@mail.com"
                  },

              prodotti:[
                {
                img:"assets/logo.png",
                nome:"penna",
                categoria:"cancelleria",
                quantitaAcquistata:100,
                skulLocation:"cnl-bic-bk-01",
                prezzo:0.30,
                quantitaRimanente:1000,
              },
              {
                img:"assets/logo.png",
                nome:"matita",
                categoria:"cancelleria",
                quantitaAcquistata:50,
                skulLocation:"cnl-bic-bk-01",
                prezzo:0.30,
                quantitaRimanente:800,
              }
              ],

              noteOrdine:{
                operatore:"mario",
                text:"Poche in magazzino, fare rifornimento al prossimo ordine"
              },

              noteCliente:{
                cliente:"fantasia",
                text:"sdognbsigujdnghosignhosgnosg nsoldikgjnowesringsoikjfgsiokedigukhnasogikjusnedog idkjgnfvmaoikgfjnosuijknhgisegujnhsoeguij jhnsoigernhsiogkshjoregujishnogiujs hnogishngirujdngsiogsneodigf jsoiguseordgishngioshn"
              },
              }
          
        },
        {
          ecommerceProvenienza:"fantasia",
          ordine: 
              {
              ecommerceProvenienza:"fantasia",
              data:"10/12/2021",
              valuta:"euro",
              corriere:"ups",
              idOrdine:"17935826",
              pagamento:"carta di credito",
              statoOrdine:"da spedire",
              totSconto:10,
              totProdotti:500,
              totSpedizione:80,
              totIncasso:400,
              chiusura:"false",
            
              indirizzo: {
                nome:"Franca",
                cognome:"Verdi",
                indirizzo1:"via san gaetano 5",
                indirizzo2:"",
                cap:"50121",
                citta:"Firenze",
                nazione:"italia",
                telefono:"6591778349"
              },

              cliente:{
                    nome:"Franca",
                    cognome:"Verdi",
                    sesso:"f",
                    email:"Francaverdi@mail.com"
                  },

              prodotti:[
                {
                img:"assets/logo.png",
                nome:"penna",
                categoria:"cancelleria",
                quantitaAcquistata:100,
                skulLocation:"cnl-bic-bk-01",
                prezzo:0.30,
                quantitaRimanente:1000,
              },
              {
                img:"assets/logo.png",
                nome:"matita",
                categoria:"cancelleria",
                quantitaAcquistata:50,
                skulLocation:"cnl-bic-bk-01",
                prezzo:0.30,
                quantitaRimanente:800,
              }
              ],

              noteOrdine:{
                operatore:"mario",
                text:"Poche in magazzino, fare rifornimento al prossimo ordine"
              },

              noteCliente:{
                cliente:"fantasia",
                text:"sdognbsigujdnghosignhosgnosg nsoldikgjnowesringsoikjfgsiokedigukhnasogikjusnedog idkjgnfvmaoikgfjnosuijknhgisegujnhsoeguij jhnsoigernhsiogkshjoregujishnogiujs hnogishngirujdngsiogsneodigf jsoiguseordgishngioshn"
              },
              }
          
        },
        {
          ecommerceProvenienza:"fantasia",
          ordine: 
              {
              ecommerceProvenienza:"fantasia",
              data:"10/12/2021",
              valuta:"euro",
              corriere:"ups",
              idOrdine:"17935826",
              pagamento:"carta di credito",
              statoOrdine:"da spedire",
              totSconto:10,
              totProdotti:500,
              totSpedizione:80,
              totIncasso:400,
              chiusura:"false",
            
              indirizzo: {
                nome:"Franca",
                cognome:"Verdi",
                indirizzo1:"via san gaetano 5",
                indirizzo2:"",
                cap:"50121",
                citta:"Firenze",
                nazione:"italia",
                telefono:"6591778349"
              },

              cliente:{
                    nome:"Franca",
                    cognome:"Verdi",
                    sesso:"f",
                    email:"Francaverdi@mail.com"
                  },

              prodotti:[
                {
                img:"assets/logo.png",
                nome:"penna",
                categoria:"cancelleria",
                quantitaAcquistata:100,
                skulLocation:"cnl-bic-bk-01",
                prezzo:0.30,
                quantitaRimanente:1000,
              },
              {
                img:"assets/logo.png",
                nome:"matita",
                categoria:"cancelleria",
                quantitaAcquistata:50,
                skulLocation:"cnl-bic-bk-01",
                prezzo:0.30,
                quantitaRimanente:800,
              }
              ],

              noteOrdine:{
                operatore:"mario",
                text:"Poche in magazzino, fare rifornimento al prossimo ordine"
              },

              noteCliente:{
                cliente:"fantasia",
                text:"sdognbsigujdnghosignhosgnosg nsoldikgjnowesringsoikjfgsiokedigukhnasogikjusnedog idkjgnfvmaoikgfjnosuijknhgisegujnhsoeguij jhnsoigernhsiogkshjoregujishnogiujs hnogishngirujdngsiogsneodigf jsoiguseordgishngioshn"
              },
              }
          
        },
        {
          ecommerceProvenienza:"fantasia",
          ordine: 
              {
              ecommerceProvenienza:"fantasia",
              data:"10/12/2021",
              valuta:"euro",
              corriere:"ups",
              idOrdine:"17935826",
              pagamento:"carta di credito",
              statoOrdine:"da spedire",
              totSconto:10,
              totProdotti:500,
              totSpedizione:80,
              totIncasso:400,
              chiusura:"false",
            
              indirizzo: {
                nome:"Franca",
                cognome:"Verdi",
                indirizzo1:"via san gaetano 5",
                indirizzo2:"",
                cap:"50121",
                citta:"Firenze",
                nazione:"italia",
                telefono:"6591778349"
              },

              cliente:{
                    nome:"Franca",
                    cognome:"Verdi",
                    sesso:"f",
                    email:"Francaverdi@mail.com"
                  },

              prodotti:[
                {
                img:"assets/logo.png",
                nome:"penna",
                categoria:"cancelleria",
                quantitaAcquistata:100,
                skulLocation:"cnl-bic-bk-01",
                prezzo:0.30,
                quantitaRimanente:1000,
              },
              {
                img:"assets/logo.png",
                nome:"matita",
                categoria:"cancelleria",
                quantitaAcquistata:50,
                skulLocation:"cnl-bic-bk-01",
                prezzo:0.30,
                quantitaRimanente:800,
              }
              ],

              noteOrdine:{
                operatore:"mario",
                text:"Poche in magazzino, fare rifornimento al prossimo ordine"
              },

              noteCliente:{
                cliente:"fantasia",
                text:"sdognbsigujdnghosignhosgnosg nsoldikgjnowesringsoikjfgsiokedigukhnasogikjusnedog idkjgnfvmaoikgfjnosuijknhgisegujnhsoeguij jhnsoigernhsiogkshjoregujishnogiujs hnogishngirujdngsiogsneodigf jsoiguseordgishngioshn"
              },
              }
          
        },
        {
          ecommerceProvenienza:"fantasia",
          ordine: 
              {
              ecommerceProvenienza:"fantasia",
              data:"10/12/2021",
              valuta:"euro",
              corriere:"ups",
              idOrdine:"17935826",
              pagamento:"carta di credito",
              statoOrdine:"da spedire",
              totSconto:10,
              totProdotti:500,
              totSpedizione:80,
              totIncasso:400,
              chiusura:"false",
            
              indirizzo: {
                nome:"Franca",
                cognome:"Verdi",
                indirizzo1:"via san gaetano 5",
                indirizzo2:"",
                cap:"50121",
                citta:"Firenze",
                nazione:"italia",
                telefono:"6591778349"
              },

              cliente:{
                    nome:"Franca",
                    cognome:"Verdi",
                    sesso:"f",
                    email:"Francaverdi@mail.com"
                  },

              prodotti:[
                {
                img:"assets/logo.png",
                nome:"penna",
                categoria:"cancelleria",
                quantitaAcquistata:100,
                skulLocation:"cnl-bic-bk-01",
                prezzo:0.30,
                quantitaRimanente:1000,
              },
              {
                img:"assets/logo.png",
                nome:"matita",
                categoria:"cancelleria",
                quantitaAcquistata:50,
                skulLocation:"cnl-bic-bk-01",
                prezzo:0.30,
                quantitaRimanente:800,
              }
              ],

              noteOrdine:{
                operatore:"mario",
                text:"Poche in magazzino, fare rifornimento al prossimo ordine"
              },

              noteCliente:{
                cliente:"fantasia",
                text:"sdognbsigujdnghosignhosgnosg nsoldikgjnowesringsoikjfgsiokedigukhnasogikjusnedog idkjgnfvmaoikgfjnosuijknhgisegujnhsoeguij jhnsoigernhsiogkshjoregujishnogiujs hnogishngirujdngsiogsneodigf jsoiguseordgishngioshn"
              },
              }
          
        },
        {
          ecommerceProvenienza:"fantasia",
          ordine: 
              {
              ecommerceProvenienza:"fantasia",
              data:"10/12/2021",
              valuta:"euro",
              corriere:"ups",
              idOrdine:"17935826",
              pagamento:"carta di credito",
              statoOrdine:"da spedire",
              totSconto:10,
              totProdotti:500,
              totSpedizione:80,
              totIncasso:400,
              chiusura:"false",
            
              indirizzo: {
                nome:"Franca",
                cognome:"Verdi",
                indirizzo1:"via san gaetano 5",
                indirizzo2:"",
                cap:"50121",
                citta:"Firenze",
                nazione:"italia",
                telefono:"6591778349"
              },

              cliente:{
                    nome:"Franca",
                    cognome:"Verdi",
                    sesso:"f",
                    email:"Francaverdi@mail.com"
                  },

              prodotti:[
                {
                img:"assets/logo.png",
                nome:"penna",
                categoria:"cancelleria",
                quantitaAcquistata:100,
                skulLocation:"cnl-bic-bk-01",
                prezzo:0.30,
                quantitaRimanente:1000,
              },
              {
                img:"assets/logo.png",
                nome:"matita",
                categoria:"cancelleria",
                quantitaAcquistata:50,
                skulLocation:"cnl-bic-bk-01",
                prezzo:0.30,
                quantitaRimanente:800,
              }
              ],

              noteOrdine:{
                operatore:"mario",
                text:"Poche in magazzino, fare rifornimento al prossimo ordine"
              },

              noteCliente:{
                cliente:"fantasia",
                text:"sdognbsigujdnghosignhosgnosg nsoldikgjnowesringsoikjfgsiokedigukhnasogikjusnedog idkjgnfvmaoikgfjnosuijknhgisegujnhsoeguij jhnsoigernhsiogkshjoregujishnogiujs hnogishngirujdngsiogsneodigf jsoiguseordgishngioshn"
              },
              }
          
        },
        {
          ecommerceProvenienza:"fantasia",
          ordine: 
              {
              ecommerceProvenienza:"fantasia",
              data:"10/12/2021",
              valuta:"euro",
              corriere:"ups",
              idOrdine:"17935826",
              pagamento:"carta di credito",
              statoOrdine:"da spedire",
              totSconto:10,
              totProdotti:500,
              totSpedizione:80,
              totIncasso:400,
              chiusura:"false",
            
              indirizzo: {
                nome:"Franca",
                cognome:"Verdi",
                indirizzo1:"via san gaetano 5",
                indirizzo2:"",
                cap:"50121",
                citta:"Firenze",
                nazione:"italia",
                telefono:"6591778349"
              },

              cliente:{
                    nome:"Franca",
                    cognome:"Verdi",
                    sesso:"f",
                    email:"Francaverdi@mail.com"
                  },

              prodotti:[
                {
                img:"assets/logo.png",
                nome:"penna",
                categoria:"cancelleria",
                quantitaAcquistata:100,
                skulLocation:"cnl-bic-bk-01",
                prezzo:0.30,
                quantitaRimanente:1000,
              },
              {
                img:"assets/logo.png",
                nome:"matita",
                categoria:"cancelleria",
                quantitaAcquistata:50,
                skulLocation:"cnl-bic-bk-01",
                prezzo:0.30,
                quantitaRimanente:800,
              }
              ],

              noteOrdine:{
                operatore:"mario",
                text:"Poche in magazzino, fare rifornimento al prossimo ordine"
              },

              noteCliente:{
                cliente:"fantasia",
                text:"sdognbsigujdnghosignhosgnosg nsoldikgjnowesringsoikjfgsiokedigukhnasogikjusnedog idkjgnfvmaoikgfjnosuijknhgisegujnhsoeguij jhnsoigernhsiogkshjoregujishnogiujs hnogishngirujdngsiogsneodigf jsoiguseordgishngioshn"
              },
              }
          
        },
        {
          ecommerceProvenienza:"fantasia",
          ordine: 
              {
              ecommerceProvenienza:"fantasia",
              data:"10/12/2021",
              valuta:"euro",
              corriere:"ups",
              idOrdine:"17935826",
              pagamento:"carta di credito",
              statoOrdine:"da spedire",
              totSconto:10,
              totProdotti:500,
              totSpedizione:80,
              totIncasso:400,
              chiusura:"false",
            
              indirizzo: {
                nome:"Franca",
                cognome:"Verdi",
                indirizzo1:"via san gaetano 5",
                indirizzo2:"",
                cap:"50121",
                citta:"Firenze",
                nazione:"italia",
                telefono:"6591778349"
              },

              cliente:{
                    nome:"Franca",
                    cognome:"Verdi",
                    sesso:"f",
                    email:"Francaverdi@mail.com"
                  },

              prodotti:[
                {
                img:"assets/logo.png",
                nome:"penna",
                categoria:"cancelleria",
                quantitaAcquistata:100,
                skulLocation:"cnl-bic-bk-01",
                prezzo:0.30,
                quantitaRimanente:1000,
              },
              {
                img:"assets/logo.png",
                nome:"matita",
                categoria:"cancelleria",
                quantitaAcquistata:50,
                skulLocation:"cnl-bic-bk-01",
                prezzo:0.30,
                quantitaRimanente:800,
              }
              ],

              noteOrdine:{
                operatore:"mario",
                text:"Poche in magazzino, fare rifornimento al prossimo ordine"
              },

              noteCliente:{
                cliente:"fantasia",
                text:"sdognbsigujdnghosignhosgnosg nsoldikgjnowesringsoikjfgsiokedigukhnasogikjusnedog idkjgnfvmaoikgfjnosuijknhgisegujnhsoeguij jhnsoigernhsiogkshjoregujishnogiujs hnogishngirujdngsiogsneodigf jsoiguseordgishngioshn"
              },
              }
          
        },
        {
          ecommerceProvenienza:"fantasia",
          ordine: 
              {
              ecommerceProvenienza:"fantasia",
              data:"10/12/2021",
              valuta:"euro",
              corriere:"ups",
              idOrdine:"17935826",
              pagamento:"carta di credito",
              statoOrdine:"da spedire",
              totSconto:10,
              totProdotti:500,
              totSpedizione:80,
              totIncasso:400,
              chiusura:"false",
            
              indirizzo: {
                nome:"Franca",
                cognome:"Verdi",
                indirizzo1:"via san gaetano 5",
                indirizzo2:"",
                cap:"50121",
                citta:"Firenze",
                nazione:"italia",
                telefono:"6591778349"
              },

              cliente:{
                    nome:"Franca",
                    cognome:"Verdi",
                    sesso:"f",
                    email:"Francaverdi@mail.com"
                  },

              prodotti:[
                {
                img:"assets/logo.png",
                nome:"penna",
                categoria:"cancelleria",
                quantitaAcquistata:100,
                skulLocation:"cnl-bic-bk-01",
                prezzo:0.30,
                quantitaRimanente:1000,
              },
              {
                img:"assets/logo.png",
                nome:"matita",
                categoria:"cancelleria",
                quantitaAcquistata:50,
                skulLocation:"cnl-bic-bk-01",
                prezzo:0.30,
                quantitaRimanente:800,
              }
              ],

              noteOrdine:{
                operatore:"mario",
                text:"Poche in magazzino, fare rifornimento al prossimo ordine"
              },

              noteCliente:{
                cliente:"fantasia",
                text:"sdognbsigujdnghosignhosgnosg nsoldikgjnowesringsoikjfgsiokedigukhnasogikjusnedog idkjgnfvmaoikgfjnosuijknhgisegujnhsoeguij jhnsoigernhsiogkshjoregujishnogiujs hnogishngirujdngsiogsneodigf jsoiguseordgishngioshn sdognbsigujdnghosignhosgnosg nsoldikgjnowesringsoikjfgsiokedigukhnasogikjusnedog idkjgnfvmaoikgfjnosuijknhgisegujnhsoeguij jhnsoigernhsiogkshjoregujishnogiujs hnogishngirujdngsiogsneodigf jsoiguseordgishngioshn"
              },
              }
          
        },
      ],
    }
  },
  methods:{
    selettore(count){
      this.countervisible = count
      console.log(this.countervisible);
    },
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
  background-color: #ffffff;
  #big-container{
    height: 100vh;
    padding: 20px;
    display: flex;
    justify-content: space-between;
  }
}

</style>
