<template>
    <v-app app>
        <v-app-bar user color="indigo darken-4">
            <NuxtLink to="/" class="text-white px-10 py-2 text-3xl ml-4 font-bold font-sans "> Jober </NuxtLink>
            <v-spacer></v-spacer>
            <NuxtLink to="/jobs" class="text-white font-sans mr-4 p-3 hover:bg-blue-600 rounded-lg">Jobs</NuxtLink>
            <NuxtLink to="/messages" class="text-white font-sans mr-4 p-3 hover:bg-blue-600 rounded-lg">Messages</NuxtLink>
            <NuxtLink to="/" class="text-white font-sans mr-4 p-3 hover:bg-blue-600 rounded-lg">Logout</NuxtLink>
        </v-app-bar>
        <v-main>
            <slot/>
        </v-main>
    </v-app>
</template>

<script setup>
</script>

<style  scoped>

</style>