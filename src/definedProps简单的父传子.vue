<template>
    
    <div>父组件</div>
     <div>父亲的钱{{money}}</div>
     <div>父亲的车{{car}}</div>
     <Son :car="car" :money="money" @parents1="newMoney"></Son>
     <h1></h1>
     <hr>
 </template>
 <script setup lang="ts">
import { ref } from 'vue';
import Son from "./components/son.vue"
     const money = ref(100)
     const car = ref("五菱宏光MINIS")
     const newMoney = (val:number)=>{
        console.log(99111119,val)
        money.value +=val
     }
 </script>