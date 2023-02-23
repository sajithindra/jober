<template>
     <v-form v-model="checkform">
            <h2 class="p-5 text-center text-indigo-600 font-mono text-2xl font-bold"> Registraion</h2>
            <v-row >
                <v-col>
                    <v-text-field label="Full Name" v-model="name" :rules="[rules.required,rules.name]" variant="underlined"></v-text-field>
                </v-col>
                <v-col>
                    <v-text-field label="Mobile" v-model="mobile" :rules="[rules.required,rules.mobile]" variant="underlined"></v-text-field>
                </v-col>
            </v-row>
            <v-row>
                <v-col>
                    <v-text-field label="Email" v-model="email" :rules="[rules.required,rules.email]" variant="underlined"></v-text-field>
                </v-col>
                <v-col>
                    <v-text-field label="Password" v-model="password" type="password" :rules="[rules.required,rules.password]" variant="underlined"></v-text-field>
                </v-col>
            </v-row>
            <v-row>
                <v-col>
                    <v-text-field label="Aadhaar" v-model="aadhaar" :rules="[rules.required,rules.aadhaar]" variant="underlined"></v-text-field>
                </v-col>
                <v-col>
                    <v-text-field label="PAN" v-model="pan" :rules="[rules.required,rules.pan]" variant="underlined"></v-text-field>
                </v-col>
            </v-row>
            <v-container class="text-center">
                <v-btn text @click="register()" color="indigo" width="30%" class="text-mono" :disabled="checkform">Register</v-btn>
            </v-container>
        </v-form>
</template>

<script setup>
const name = ref("");
const email = ref("");
const password = ref("");
const mobile = ref("");
let checkform=false;
const aadhaar = ref("");
const pan = ref("");

let rules = {
    required: (v) => !!v || "Required",
    name : (v) => (v.match(/^[a-zA-Z\. ]+$/)) || "Please check name",
    mobile : (v) => (v.match(/^[789]\d{9}$/)) || "Please check mobile number",
    password : (v) => (v.length >=8) || "Minimum 8 charactors required",
    email : (v) => (v.match(/^[\w-\.]+@([\w-]+\.)+[\w-]{2,4}$/)) || "Please check email",
    aadhaar : (v) => (v.match(/^[0-9]\d{12}$/)) || "Check aadhaar number",
    pan: (v)=> (v.match(/^[A-Z]{5}[0-9]{4}[A-Z]{1}$/)) || "Check PAN number"
}
async function register() {
    let user = {
        name : name.value,
        email : email.value,
        password : password.value,
        mobile : mobile.value,
        aadhaar : aadhaar.value,
        pan : pan.value
    }
    console.log(user)

}
</script>

<style scoped>

</style>