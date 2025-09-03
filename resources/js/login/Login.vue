<script lang="ts">
import { ref } from 'vue';


const user = ref({
    name:'',
    password:''
}) 

const submit = () =>{};
</script>
<template>
    <form>
        <input v-model="user.name" required type="text"></input>
        <input v-model="user.password" required type="password"></input>
        <button @click="submit"></button>
    </form>
</template>