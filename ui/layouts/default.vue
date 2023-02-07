<template>
  <v-app dark>
    <v-app-bar fixed app color="indigo darken-2">
     
      <v-toolbar-title >Jober</v-toolbar-title>
      <v-spacer></v-spacer>
      <v-btn text color="white"> Jobs</v-btn>
      <v-btn text color="white"> companies</v-btn>
      <v-btn text color="white"> Services </v-btn>
      <v-btn text color="white"> Register</v-btn>
    </v-app-bar>
    <v-main>
      <v-container >
        <Nuxt />
      </v-container>
    </v-main>

    <v-footer
      app
    >
      <span>&copy; {{ new Date().getFullYear() }}</span>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  name: 'DefaultLayout',
  data () {
    return {
      clipped: false,
      drawer: false,
      fixed: false,
      items: [
        {
          icon: 'mdi-apps',
          title: 'Welcome',
          to: '/'
        },
        {
          icon: 'mdi-chart-bubble',
          title: 'Inspire',
          to: '/inspire'
        }
      ],
      miniVariant: false,
      right: true,
      rightDrawer: false,
      title: 'Vuetify.js'
    }
  }
}
</script>
