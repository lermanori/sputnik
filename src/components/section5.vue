<template>
  <div class="pt-3 pb-8" :style="{backgroundColor:'rgb(241,90,36)',minHeight:'50vh'}">
    <h4 class="pl-3 white--text">MAKE A RESERVATION</h4>
    <app-form />
  </div>
</template>

<script>
import appForm from "../components/appForm";
export default {
  components: {
    "app-form": appForm
  }
  // data() {
  //   };
};
</script>

<style scoped>
</style>