<template>
     <v-form>
            <h2 class="p-5 text-center text-indigo-600 font-sans text-2xl font-bold"> Candidate Registraion</h2>
            <v-row >
                <v-col>
                    <v-text-field label="Full Name" v-model="name" :rules="[rules.required]"></v-text-field>
                </v-col>
                <v-col>
                    <v-text-field label="Mobile" v-model="mobile" :rules="[rules.required]"></v-text-field>
                </v-col>
            </v-row>
            <v-row>
                <v-col>
                    <v-text-field label="Email" v-model="email" :rules="[rules.required]"></v-text-field>
                </v-col>
                <v-col>
                    <v-text-field label="Password" v-model="password" type="password" :rules="[rules.required]"></v-text-field>
                </v-col>
            </v-row>
            <v-row>
                <v-col>
                    <v-text-field label="Aadhaar" v-model="aadhaar" :rules="[rules.required]"></v-text-field>
                </v-col>
                <v-col>
                    <v-text-field label="PAN" v-model="pan" :rules="[rules.required]"></v-text-field>
                </v-col>
            </v-row>
            <v-container class="text-center">
                <v-btn text @click="register()" color="indigo" width="30%" class="text-mono">Register</v-btn>
            </v-container>
        </v-form>
</template>

<script setup>
const name = ref("");
const email = ref("");
const password = ref("");
const mobile = ref("");
const aadhaar = ref("");
const pan = ref("");

let rules = {
    required: (v) => !!v || "Required",
    mobile  : (v) => !!v || "Mobile",
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