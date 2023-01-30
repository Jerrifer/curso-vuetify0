<template>
  <v-app>
    <v-toolbar app class="info">

      <v-app-bar-nav-icon @click="drawer = !drawer"></v-app-bar-nav-icon>

        <v-toolbar-title>Vuetify</v-toolbar-title>

        <v-spacer></v-spacer>
        <v-btn class="success">
          Ingreso
        </v-btn>
        <v-btn class="error">
          Salir
        </v-btn>

    </v-toolbar>

    <v-navigation-drawer
        app
        class="secondary" 
        v-model="drawer" 
        temporary>

        <v-layout mt-4 column align-center>
          <v-flex>
            <v-avatar>
              <img src="https://randomuser.me/api/portraits/men/78.jpg" alt="">
            </v-avatar>
          </v-flex>
          <v-flex>
            <p class="white--text mt-3 headline">Juan Lopez</p>
          </v-flex>
        </v-layout>

    </v-navigation-drawer>
    <v-main>
      <router-view/>
    </v-main>
  </v-app>
</template>

<script>

export default {
  name: 'App',

  data: () => ({
    drawer: true
  }),
};
</script>
