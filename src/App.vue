<template>
  <div class="bg-trasparent  w-screen h-16 flex items-center justify-center ">
    <div class="flex items-center animate__animated animate__backInLeft text-white font-bold
      mx-8 bg-gray-100 bg-opacity-10 hover:bg-gray-200 hover:bg-opacity-40 h-full px-5
       cursor-pointer text-2xl">
      <router-link  to="/">Home</router-link> 
    </div>
    <div class="flex items-center animate__animated animate__backInRight text-white font-bold
      mx-8 bg-gray-100 bg-opacity-10 hover:bg-gray-200 hover:bg-opacity-40 h-full px-5
       cursor-pointer text-2xl">
      <router-link  to="/about">Otro</router-link>
    </div>
  </div>
  <router-view/>
</template>

<style>
</style>
