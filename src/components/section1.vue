<template>
  <div style="background-color:black;">
    <v-carousel
      cycle
      height="400"
      hide-delimiter-background
      class="opacity-in"
      :interval="9000000"
      :hide-delimiters="true"
      :show-arrows="false"
    >
      <v-carousel-item v-for="(slide, i) in slides" :key="i">
        <v-img contain position="center top" :src="slide" style="max-height:70vh"></v-img>
      </v-carousel-item>
    </v-carousel>
    <!-- <app-3d-model /> -->
  </div>
</template>

<script>
import app3dModel from "../components/p53dmodel.vue";
export default {
  components: {
    "app-3d-model": app3dModel
  },
  data() {
    return {
      colors: [
        "indigo",
        "warning",
        "pink darken-2",
        "red lighten-1",
        "deep-purple accent-4"
      ],
      slides: [
        require("../assets/section1Img.jpg"),
        require("../assets/section1Img2.jpg")
      ]
    };
  }
};
</script>

<style scoped>
.opacity-in {
  animation-name: opacity;
  animation-duration: 2s;
  animation-delay: 3s;
  animation-fill-mode: forwards;
  opacity: 0.1;
}
@keyframes opacity {
  from {
    opacity: 0.1;
  }
  to {
    opacity: 1;
  }
}
</style>