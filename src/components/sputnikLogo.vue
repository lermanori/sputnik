<template>
  <div>
    <img :src="require('../assets/Sputnik_Logo.png')" class="logo-animation" />
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
.logo-animation {
  position: absolute;
  animation-name: logoMovement;
  animation-duration: 4s;
  animation-fill-mode: forwards;
  width: 40px;
  height: 40px;
  top: 5px;
  left: 5px;
}
@keyframes logoMovement {
  0% {
    transform: translateY(60vw) translateX(40vw) scale(6) rotate(359deg);
    /* transform: ; */
    /* transform: scale(5); */
  }
  70% {
    transform: translateY(60vw) translateX(40vw) scale(6) rotate(0deg);
  }
  100% {
    /* transform: scale(1); */
    transform: scale(1) translateY(0px) translateX(0px);
    /* transform: translateX(0px); */
  }
}
</style>