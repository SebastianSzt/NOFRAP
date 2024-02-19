<template>
    <div>
      <h1>Lista użytkowników</h1>
      <div v-for="user in users" :key="user.id" class="business-card">
        <h2>{{ user.name }}</h2>
        <p><b>Username:</b> {{ user.username }}</p>
        <p><b>Email:</b> {{ user.email }}</p>
        <p><b>Address:</b> {{ user.address.street }}, {{ user.address.suite }}, {{ user.address.city }}, {{ user.address.zipcode }} <br /> {{ user.address.geo.lat }}, {{ user.address.geo.lng }} </p>
        <p><b>Phone:</b> {{ user.phone }}</p>
        <p><b>Website:</b> {{ user.website }}</p>
        <p><b>Company:</b> {{ user.company.name }} - {{ user.company.catchPhrase }} - {{ user.company.bs }}</p>
      </div>
    </div>
</template>
  
<script>
    const url  = new URL("https://jsonplaceholder.typicode.com/users");
    export default {
        data() {
            return {
                users: [],
            };
        },
        mounted() {
            this.fetchUserData();
        },
        methods: {
            async fetchUserData() {
                try {
                    const response = await fetch(url);
                    const data = await response.json();
                    this.users = data;
                } catch (error) {
                    console.error('Error fetching user data:', error);
                }
            },
        },
    };
</script>
  
<style scoped>
    .business-card {
        border: 1px solid #ccc;
        padding: 10px;
        margin-top: 10px;
        border-radius: 8px;
        box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
        min-width: 150px;
    }
</style>