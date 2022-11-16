<template>
    
   <div>{{user}}</div>
    <button @click="user.age++">点击增加年龄</button>
    
</template>
<script setup lang="ts">
    import {ref ,watch} from "vue"
    const user = ref({
        name:"zs",
        age:18
    })
    watch(user,(val,oldval)=>{
        console.log("执行了",val,oldval)
    },{deep:true,immediate:true})
    
</script>