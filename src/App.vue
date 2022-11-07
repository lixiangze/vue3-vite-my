<template>
    
    <p>{{number}}</p>
    <button @click="eventDiji">点击</button>
</template>
<script setup lang="ts">
import {ref} from "vue"
    const number = ref(10)
    const eventDiji = ()=>{
        number.value +=1 
    }
    
</script>