<template>
    <div>子组件</div>
    <div>使用父亲的钱{{money}}</div>
    <div>使用父亲的车{{car}}</div>
    <button @click="parents1">新增钱</button>
</template>
<script setup lang="ts">
import { inject, Ref } from 'vue';


    
    const emit = defineEmits(["parents1"])
    const parents1 = ()=>{
        console.log(emit)
        emit("parents1",10000)
        console.log(9999)
    }
   const money =  inject<Ref<number>>("money")
   const car = inject<Ref<string>>("car")
</script>