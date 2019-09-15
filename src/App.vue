<template>
  <v-app>
    <v-app-bar app :style="{width:'100vw',backgroundColor:'black'}">
      <v-toolbar-title class="headline text-uppercase">
        <sputnik-logo />
      </v-toolbar-title>
      <v-spacer></v-spacer>
      <v-btn text href="https://github.com/vuetifyjs/vuetify/releases/latest" target="_blank">
        <span class="mr-2">Latest Release</span>
      </v-btn>
    </v-app-bar>

    <v-content>
      <router-view />
    </v-content>
  </v-app>
</template>

<script>
import sputnikLogo from "./components/sputnikLogo";

export default {
  name: "App",
  components: {
    sputnikLogo
  },
  data: () => ({
    //
  })
};
</script>
