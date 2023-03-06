<template>
 <v-app app>
    <v-app-bar bar color="indigo darken-4" elevation="4">
        <NuxtLink to="/" class="text-white px-10 py-2 text-3xl ml-4 font-bold font-sans "> Jober </NuxtLink>
        <v-spacer></v-spacer>
        <NuxtLink to="/jobs" class="w-20  text-center text-white font-sans p-3 mr-4 hover:bg-blue-600 rounded-lg">Jobs</NuxtLink>
        <NuxtLink to="/companylogin" class="text-white font-sans mr-4 p-3 hover:bg-blue-600 rounded-lg">Companies</NuxtLink>
        <NuxtLink to ="/register" class="text-white font-sans mr-4 p-3 hover:bg-blue-600 rounded-lg" >Register</NuxtLink>
    </v-app-bar>
    <v-main>
        <slot/>
    </v-main>
    <v-footer padless>
    <v-col
      class="text-center text-indigo-500 px-10 py-2 text-l"
      cols="12"
    >
      {{ new Date().getFullYear() }} : <strong>Copyright (c) Securekloud Technologies, Ltd. All rights reserved.</strong>
    </v-col>
  </v-footer>
 </v-app>
</template>

<script setup>

</script>

<style scoped>

</style>