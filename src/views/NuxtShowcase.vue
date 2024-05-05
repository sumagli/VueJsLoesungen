<script setup>
import { ref } from 'vue';

// Reactive reference for users
const users = ref([]);

// Function to fetch users
async function fetchUsers() {
    try {
        const response = await fetch('https://jsonplaceholder.typicode.com/users');
        users.value = await response.json(); // Assuming the response is an array of users
    } catch (error) {
        console.error('Error fetching users:', error);
        users.value = [];
    }
}
fetchUsers();


</script>

<template>
    <div>
        <h1>Server-Side Rendered Page</h1>
        <p>This pages data was fetched on the server:</p>
        <ul>
            <li v-for="user in users" :key="user.id">name:{{ user.name }}, email:{{ user.email }}</li>
        </ul>
    </div>
</template>
