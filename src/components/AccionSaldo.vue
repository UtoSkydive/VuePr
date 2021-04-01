<template>
  <!-- <button @click="this.$emit('accion')">{{text}}</button> -->
  <button @click="accion" :disabled="desactivar">{{text}}</button>
</template>

<script>
export default {
    props:{
        text:String,
        desactivar:{
            type: Boolean,
            default:false
        }
    },
    methods:{
        accion(){
            this.$emit('accion')
        }
    }
}
</script>

<style>

</style>
