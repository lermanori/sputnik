<template>
  <div class="pa-4" :style="{backgroundColor:'black',minHeight:'5vh'}">
    <v-layout justify-space-between>
      <v-flex xs5>
        <h5 class="white--text pt-3">Allenby 122, Tel Aviv.</h5>
      </v-flex>
      <v-flex xs7>
        <v-layout class="pt-1">
          <v-flex xs6>
            <v-btn outlined dark style="color:rgb(241,90,36)">instagram</v-btn>
          </v-flex>
          <v-flex xs6>
            <v-btn outlined dark style="color:rgb(241,90,36)">facebook</v-btn>
          </v-flex>
        </v-layout>
      </v-flex>
    </v-layout>
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