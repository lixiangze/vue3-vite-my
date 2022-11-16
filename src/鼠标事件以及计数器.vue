<template>
    
    <p>{{move.x}}</p>
    <p>{{move.y}}</p>
    <p>{{number}}</p>
    <button @click="number++">加1事件</button>
</template>
<script setup lang="ts">
import {onMounted, onUnmounted, reactive, ref} from "vue"
    const move = reactive({
        x:0,
        y:0
    })
    const mouse = (e:MouseEvent)=>{
        move.x = e.clientX;
        move.y = e.clientY;
    }
    const number = ref(10)
    onMounted(()=>{
        document.addEventListener("mousemove",mouse)
    })
    onUnmounted(()=>{
        document.removeEventListener("mousemove",mouse)
    })
</script>