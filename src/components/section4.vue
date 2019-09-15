<template>
  <div class="text-center" :style="{backgroundColor:'black',minHeight:'70vh'}">
    <h1 class="white--text text-center pt-3" style="text-decoration:underline">FOOD & DRINK MENU</h1>
    <v-btn
      class="my-3"
      @click="english = !english"
      style="background-color:rgb(241,90,36);"
    >{{english?'HEBREW':'ENGLISH'}}</v-btn>
    <v-carousel v-if="english" hide-delimiters>
      <v-carousel-item v-for="(menu, i) in englishMenu" :key="'u'+i">
        <v-img :src="menu"></v-img>
      </v-carousel-item>
    </v-carousel>
    <v-carousel v-if="!english" hide-delimiters>
      <v-carousel-item v-for="(menu, i) in HebrewMenu" :key="'d'+i">
        <v-img :src="menu"></v-img>
      </v-carousel-item>
    </v-carousel>
  </div>
</template>

<script>
export default {
  data() {
    return {
      english: false,
      englishMenu: [
        require("../assets/english_menu.jpg"),
        require("../assets/english_menu2.jpg")
      ],
      HebrewMenu: [
        require("../assets/hebrew_menu.jpg"),
        require("../assets/hebrew_menu2.jpg")
      ]
    };
  }
};
</script>

<style scoped>
</style>