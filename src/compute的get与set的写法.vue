<template>
    
    <div>我今年的年龄<input type="text" v-model="age"></div>
    <div>我明年的年龄<input type="text" v-model="nextAge"></div>
    <div>我后年的年龄<input type="text" v-model="nextToNextAge"></div>
    
</template>
<script setup lang="ts">
import {ref,computed} from "vue"
    let age = ref(0)
    // if(age.value<0){
    //     age.value = 0
    //     alert("年龄不能小于0")   
    // }
    // age = computed({

    // }) 
    const nextAge = computed({
        get:()=>{
            return age.value-0+1 
        },
        set(value:number){
            age.value = value-1
        }
    })
    const nextToNextAge = computed({
        get:()=>{
            return age.value-0+2 
        },
        set(value:number){
            age.value = value-2
        }
    })
</script>