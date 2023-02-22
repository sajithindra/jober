<template>
    <v-container style="width: 50%;">
        <v-text-field label="search..." v-model="post" variant="underlined"></v-text-field>
        <v-container style="width: 30%;">
            <v-btn @click="search()"  color="indigo darken-2" class="text-white font-sans text-bold"> Search</v-btn>
        </v-container>
    </v-container>
</template>

<script setup>
const post = ref("")
async function search(){

}
</script>

<style lang="scss" scoped>

</style>