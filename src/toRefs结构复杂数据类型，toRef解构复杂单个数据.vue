<template>
    
   <div>{{user}}</div>
    <button @click="age++">点击增加年龄</button>
    <button @click="name+='啊'">点击增加啊一下</button>
</template>
<script setup lang="ts">
    import {ref ,toRefs,watch} from "vue"
    const user = ref({
        name:"zs",
        age:18
    })
    // watch(user,(val,oldval)=>{
    //     console.log("执行了",val,oldval)
    // },{deep:true,immediate:true})
    // watch(()=>user.value.name,(val)=>{console.log(9999)})
        const {name,age} = toRefs(user.value)
</script>