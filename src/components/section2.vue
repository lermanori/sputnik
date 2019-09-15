<template>
  <app-sputnik-love />
</template>

<script>
import sputnikLove from "../components/sputnikLove.vue";
import app3dModel from "../components/p53dmodel.vue";
export default {
  components: {
    "app-3d-model": app3dModel,
    "app-sputnik-love": sputnikLove
  }
};
</script>

<style scoped>
</style>