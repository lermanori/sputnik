<template>
  <div>
    <app-section1 />
    <app-section2 />
    <app-section3 :slides="slides" />
    <app-section4 />
    <app-section5 />
    <app-section6 />
    <app-footer />
  </div>
</template>

<script>
import section1 from "../components/section1.vue";
import section2 from "../components/section2.vue";
import section3 from "../components/section3.vue";
import section4 from "../components/section4.vue";
import section5 from "../components/section5.vue";
import section6 from "../components/section6.vue";
import appFooter from "../components/appFooter.vue";
export default {
  components: {
    "app-section1": section1,
    "app-section2": section2,
    "app-section3": section3,
    "app-section4": section4,
    "app-section5": section5,
    "app-section6": section6,
    "app-footer": appFooter
  },
  data() {
    return {
      slides: [
        {
          src: require("../assets/section1Img.jpg"),
          text: "lorem ipsum dolor emmet"
        },
        {
          src: require("../assets/section1Img2.jpg"),
          text: "lorem ipsum dolor emmet"
        }
      ]
    };
  }
};
</script>

<style scoped>
</style>