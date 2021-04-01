<template>
  <h2>Tipo de cuenta: {{cuenta}} </h2>
  <h2>{{saldo}}</h2>
  <h2>Cuenta {{ estado ? 'Activa' : 'Desactivada'}}</h2>
 <!-- <div v-for="(item,index) in servicios" :key="index">
     {{index+1}} - {{item}}
 </div> -->
 <div v-for="(item,index) in servicios" :key="index">
      {{index+1}} -  {{ item }}
 </div>
 <accion-saldo text="Aumentar Saldo" @accion="aumentar"></accion-saldo>
 <accion-saldo text="Disminuir Saldo" :disabled="desactivar" @accion="dsiminuir"></accion-saldo>
 <accion-saldo text="Multiplicar saldo" @accion="multiplicar"></accion-saldo>
 <accion-saldo text="dividir saldo" @accion="dividir" :disabled="desactivar"></accion-saldo>
</template>

<script>
import AccionSaldo from './AccionSaldo.vue'
export default {
  components: { AccionSaldo },
    data(){
        return{
            saldo:1000,
            cuenta: 'Visa',
            estado:false,
            servicios : ['giro','abono','transferencias'],
            desactivar :false
        }
    },
    methods:{
        aumentar(){
            this.saldo = this.saldo+100;
            this.desactivar = false;

        },
        dsiminuir(){
            if(this.saldo == 0){
                this.desactivar = true;
                alert('saldo agotado');
                return;
            }
            this.saldo = this.saldo-100

        },
        multiplicar(){
            this.saldo *= 2;
        },
        dividir(){
            if(this.saldo == 0){
                this.desactivar = true;
                alert('saldo agotado');
                return;
            }
            this.saldo /= 100;
        }
    }
}
</script>

<style>

</style>