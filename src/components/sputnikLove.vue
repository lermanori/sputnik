<template>
  <div class="cursor-circle-black" :style="{height:'50vh',width:'100%'}">
    <section class :style="{height:'50%',backgroundColor:'black'}">
      <v-img contain :src="require('../assets/sput.png')" class="rotation blend" />
    </section>
    <section :style="{height:'50%',backgroundColor:'white'}"></section>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
.cursor-circle-black {
  cursor: url("/round.png");
}
.blend {
  mix-blend-mode: difference;
  height: 50vh;
}
.rotation {
  animation-name: rotate;
  animation-duration: 4s;
  animation-fill-mode: forwards;
  animation-iteration-count: infinite;
}
@keyframes rotate {
  from {
    transform: rotate(0deg);
  }
  to {
    transform: rotate(359deg);
  }
}
</style>