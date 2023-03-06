<template>
    <v-container style="width:75%;">
        <v-form v-model="formValid" class="p-6 ">
            <h1 class="p-4 text-center text-indigo-600 text-3xl font-bold font-mono" > Login </h1>
            <v-text-field label="Username" v-model="username" :rules="[rules.required]" variant="underlined"></v-text-field>
            <v-text-field label="Password" v-model="password" type="password" :rules="[rules.required,rules.password]" variant="underlined"></v-text-field>
            <v-container class="text-center">
                <v-btn text @click="signin()" width="50%" color="indigo" class="font-mono"> Login </v-btn>
            </v-container>
        </v-form>
    </v-container>
</template>

<script setup lang="ts">
let formValid = ref(false);
const username = ref("");
const password = ref("");
let rules ={
    required : (v: any) => !!v || "required",
    password : (v: any) => (v.length >= 8 ) || "Minimum 8 Characters are required",

}
async function signin() { console.log(formValid.value)}
</script>

<style  scoped>

</style>