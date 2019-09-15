<template>
  <div class :style="{backgroundColor:'black'}">
    <h2
      class="ml-2 pa-5"
      :style="{color:'rgb(241,90,36)',fontSize:'1em',textDecoration:'underline',textUnderlinePosition: 'under',
    textDecorationColor: 'antiquewhite'}"
    >
      <span>EVENTS</span>
    </h2>
    <v-window :show-arrows="true" v-model="onboarding" dark style="max-height:70vh">
      <v-window-item v-for="(slide,n) in slides" :key="`card-${n}`">
        <v-card class="mx-auto" max-width="344" style="background-color:#111111">
          <v-img :src="slide.src" height="200px"></v-img>
          <v-card-actions>
            <v-btn class="mx-auto" icon @click="show = !show" style="background-color:#111111">
              <v-icon>{{ show ? 'mdi-chevron-up' : 'mdi-chevron-down' }}</v-icon>
            </v-btn>
          </v-card-actions>

          <v-expand-transition>
            <div v-show="show">
              <v-card-text>{{slide.text}}</v-card-text>
              <v-btn class="mx-auto mb-5" :to="slide.eventUrl" color="red" style="width:100%">EVENT</v-btn>
            </div>
          </v-expand-transition>
        </v-card>
      </v-window-item>
    </v-window>
  </div>
</template>

<script>
import sputnikLove from "../components/sputnikLove.vue";
import app3dModel from "../components/p53dmodel.vue";
export default {
  components: {
    "app-3d-model": app3dModel,
    "app-sputnik-love": sputnikLove
  },
  props: ["slides"],
  data() {
    return {
      length: 3,
      onboarding: 0,
      show: false
    };
  },
  methods: {
    next() {
      this.onboarding =
        this.onboarding + 1 === this.length ? 0 : this.onboarding + 1;
    },
    prev() {
      this.onboarding =
        this.onboarding - 1 < 0 ? this.length - 1 : this.onboarding - 1;
    }
  }
};
</script>

<style scoped>
</style>