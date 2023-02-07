<template>
     <v-container style="width: 30%;">
    <v-form v-model="loginForm">
      <h1 class="text-center">Candidate Login</h1>
      <v-text-field v-model="username" label="Username"></v-text-field>
      <v-text-field v-model="password" label="Password"></v-text-field>
      <v-container class="text-center">
          <v-btn text @click="signin()" width="200px">LogIn</v-btn>
      </v-container>
  </v-form>
  </v-container>
</template>
<script >
export default {
    name: "login",
    data:() =>({
        username : "",
        password : "",
    }),
}
</script>