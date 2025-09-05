<script lang="ts">
import axios from 'axios';
import { ref } from 'vue';


const user = ref({
    name:'',
    password:''
});

const login = () =>{
    axios.get('/sanctum/csrf-cookie').then(response =>{
        
    });
};

</script>

<template>
    <form v-on:submit.prevent="login">
        <input v-model="user.name" required type="text"></input>
        <input v-model="user.password" required type="password"></input>
        <button type="submit"></button>
    </form>
</template>