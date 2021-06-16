<template>
  <div class="absolute z-50 bg-trasparent  w-screen h-8 md:h-16 flex items-center justify-between ">
    <div class="text-white text-sm md:text-3xl md:font-bold ml-6 animate__animated animate__fadeInDown">CBIMULTIASSETS</div>
    <div class="flex items-center md:w-auto  justify-end md:justify-between">
      <div class="flex items-center animate__animated animate__backInLeft text-white font-bold
      mx-1 md:mx-8 bg-gray-100 bg-opacity-10 hover:bg-gray-200 hover:bg-opacity-40 h-full px-5
       cursor-pointer text-xs md:text-2xl">
      <router-link  to="/">Home</router-link> 
    </div>
    <div class="flex items-center animate__animated animate__backInRight text-white font-bold
      mx-1 md:mx-8 bg-gray-100 bg-opacity-10 hover:bg-gray-200 hover:bg-opacity-40 h-full px-5
       cursor-pointer text-xs md:text-2xl">
      <router-link  to="/about">Otro</router-link>
    </div>
    </div>
  </div>
  <router-view/>
</template>

<style>
</style>
