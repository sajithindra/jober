<template>
    <v-container style="width: 50%;">
        <v-text-field label="search..." v-model="position" variant="underlined"></v-text-field>
        <v-container style="width: 30%;">
        <v-btn @click="search()"  color="indigo darken-2" class="text-white font-sans text-bold"> Search</v-btn>
        </v-container>
    </v-container>
</template>

<script setup>
let position = ref(false)
async function search(){
    console.log(this.position)
}
</script>

<style lang="scss" scoped>

</style>