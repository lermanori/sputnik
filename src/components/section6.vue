<template>
  <div class :style="{backgroundColor:'black',minHeight:'40vh'}">
    <h1 class="white--text text-center" style="transform: translateY(-22px);">ABOUT</h1>
    <v-carousel hide-delimiters :height="375">
      <v-carousel-item v-for="(img, i) in about" :key="'d'+i">
        <v-img :src="img"></v-img>
      </v-carousel-item>
    </v-carousel>
    <p class="white--text pt-5 mb-0 pb-5">{{aboutText}}</p>
  </div>
</template>

<script>
export default {
  components: {},
  data() {
    return {
      about: [
        require("../assets/section1Img.jpg"),
        require("../assets/section1Img2.jpg")
      ],
      aboutText: "hello lorem ipsum dolor emmet"
    };
  }
};
</script>

<style scoped>
</style>