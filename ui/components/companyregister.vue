<template>
   <v-container style="width:3siro0%">
        <v-form > 
            <v-container style="padding: 50px%;">
                <h3 class="text-indigo-600 font-mono text-center font-extrabold">Enterprise Registration</h3>
            </v-container>
            <v-container style="padding: 50px">
            <v-text-field label="Name " variant="underlined" v-model="name" :rules="[rules.required]"></v-text-field>
            <v-text-field label="Email" variant="underlined" v-model="email" :rules="[rules.required]"></v-text-field>
            <v-text-field label="Mobile" variant="underlined" v-model="mobile" :rules="[rules.required,rules.mobile]"></v-text-field>
            <v-text-field label="Password" v-model="password" type="password" :rules="[rules.required,rules.password]" variant="underlined"></v-text-field>
            <v-text-field label="Company Name" variant="underlined" v-model="companyname" :rules="[rules.required]"></v-text-field>
            <v-text-field label="CIN" variant="underlined" v-model="cin" :rules="[rules.required]"></v-text-field>
            <v-container style="width:50%" class="text-center">
                <v-btn @click="forward()" color="indigo darken-2" class="text-white font-mono">Register</v-btn>
            </v-container>
        </v-container>
        </v-form>
   </v-container>
</template>

<script setup>
const companyname = ref("")
const email=ref("")
const password= ref("")
const name= ref("")
const mobile=ref("")
const cin=ref("")
let rules = {
    required : (v) => !!v || "required",
    password : (v) => (v.length >= 8 ) || "Minimum 8 Characters are required",
    mobile : (v) => (v.length == 10  ) || "Mobile number is wrong"
}
const gstnumber=ref("")
function forward(){
    console.log("inside forward function")
}
</script>

<style lang="scss" scoped>

</style>