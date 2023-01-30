<template>
  <v-app>

    <v-card
      color="grey lighten-4"
      flat
      title
    >
      <v-toolbar app class="info" dense>

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
    </v-card>
   


    <v-navigation-drawer
        app
        class="secondary" 
        v-model="drawer" 
        temporary>

        <v-layout mt-4 column align-center>
          <v-flex>
            <v-avatar>
              <img src="https://randomuser.me/api/portraits/men/85.jpg">
            </v-avatar>
          </v-flex>
          <v-flex>
            <p class="white--text mt-3 headline">Juan Lopez</p>
          </v-flex>
        </v-layout>

        <v-layout column>
          <v-flex mx-3>
            <v-btn my-2 :to="{name: 'home'}" color="success" block>Home</v-btn>
            <v-btn :to="{name: 'tasks'}" color="success" block>Tasks List</v-btn>
          </v-flex>
        </v-layout>

    </v-navigation-drawer>
    <v-main>
      <router-view/>
    </v-main>
  </v-app>
</template>
<!-- <template>
  <div>
    <v-toolbar
      dark
      prominent
      src="https://cdn.vuetifyjs.com/images/backgrounds/vbanner.jpg"
    >
      <v-app-bar-nav-icon></v-app-bar-nav-icon>

      <v-toolbar-title>Vuetify</v-toolbar-title>

      <v-spacer></v-spacer>

      <v-btn icon>
        <v-icon>mdi-export</v-icon>
      </v-btn>
    </v-toolbar>
  </div>
</template> -->
<script>

export default {
  name: 'App',

  data: () => ({
    drawer: false
  }),
};
</script>

<!-- <style  scoped>
.success{
  margin: 4px;
}
.error{
  margin: 4px
}
</style> -->


