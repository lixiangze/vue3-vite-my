<template>
    <div>
        {{msg.name}}
    </div>
    <p>{{money}}</p>
    <button @click="eventDiji">点击</button>
</template>
<script lang="ts">
import { defineComponent ,reactive,ref} from 'vue';

export default defineComponent({
    setup(){
        let msg = reactive({
            name:"zhangsan",
            age:18
        });
        let money = ref(1000)
        let eventDiji = ()=>{
            msg.name="nest",
            money.value = 200
        }
        return {msg ,eventDiji,money}
    }
})
</script>