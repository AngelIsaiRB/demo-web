<template>
  <div class="h-screen flex items-center">
      <div class="ml-2 md:ml-40">
          <p class="text-black font-bold text-2xl md:text-8xl ">REVOLUCIONAMOS </p>          
          <p class="invisible md:visible text-black font-bold text-2xl md:text-8xl textanimated">INVERSIONES</p>
          <p class="visible md:invisible -mt-6 text-black font-bold text-2xl md:text-8xl textanimatedphone">INVERSIONES</p>
          
      </div>
  </div>
</template>

<script>
import gsap from "gsap";
export default {
mounted () {
    gsap.to(".textanimated", {duration: 2, x: 300});
    gsap.to(".textanimatedphone", {duration: 2, x: 75});
    gsap.to(".box", {
  scrollTrigger: ".box", // start the animation when ".box" enters the viewport (once)
  y: 500
});
},
}
</script>

<style>

</style>