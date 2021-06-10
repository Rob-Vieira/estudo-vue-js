<template>
  <div id="app">
    <h1>Guia Clientes</h1>
    <Cliente :cliente="cliente01" :show="true" :isPremium="true"/>
    <Cliente :cliente="cliente02" :show="true"/>
    <Cliente :cliente="cliente03" :show="false"/>
    <Cliente :cliente="cliente01" :show="true"/>
  </div>
</template>

<script>
import Cliente from './components/Cliente'

export default {
  name: 'App',
  components: {
    Cliente
  },
  data(){
    return{
      cliente01: {
        nome: "Robson Vieira",
        idade: 21,
        cel: 992033717,
        end: "Barra Mansa - RJ",
        email: "robson@gmail.com",
        desc: "Nosso melhor cliente."
      },
      cliente02: {
        nome: "Jorge goge",
        idade: 32,
        cel: 996453717,
        end: "Barra Mansa - RJ",
        email: "jorge@gmail.com",
        desc: "Nosso melhor cliente."
      },
      cliente03: {
        nome: "Biatriz Vonce",
        idade: 200,
        cel: 993343717,
        end: "Barra Mansa - RJ",
        email: "bia@gmail.com",
        desc: "Nosso melhor cliente."
      }
    }
  }
}
</script>

<style>
</style>
