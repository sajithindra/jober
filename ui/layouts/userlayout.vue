<template>
    <v-app app>
        <v-app-bar user color="indigo darken-4">
            <v-btn icon><Icon name="mdi-account" size="30px"/></v-btn>
            <NuxtLink to="/" class="text-white py-2 text-xl ml-4 font-bold font-sans "> {{ name }} </NuxtLink>
            <v-spacer></v-spacer>
            <NuxtLink to="/jobs" class="text-white font-sans mr-4 p-3 hover:bg-blue-600 rounded-lg">Jobs</NuxtLink>
            <NuxtLink to="/mail" class="text-white font-sans mr-4 p-3 hover:bg-blue-600 rounded-lg">Mail</NuxtLink>
            <NuxtLink to="/" class="text-white font-sans mr-4 p-3 hover:bg-blue-600 rounded-lg">Logout</NuxtLink>
        </v-app-bar>
        <v-main>
            <slot/>
        </v-main>
    </v-app>
</template>

<script setup>
const name = "John Doe"
</script>

<style  scoped>

</style>