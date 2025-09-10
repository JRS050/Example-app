<script setup lang="ts">
import axios from 'axios';
import { computed } from 'vue';

const fetchUserData = async () => {
  try {
    const response = await axios.get('/api/me');
    console.log('User Data:', response.data);
    return response;
   
  } catch (error) {
    console.error('Error fetching user data:', error);
    return error;
  }
};
const user = computed(()=>fetchUserData());

</script>
<template>
    <p>{{ user }}</p>
</template>