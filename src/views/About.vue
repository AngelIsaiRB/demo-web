<template>
  <headMenuComponentVue/>
  <Otro3dDemoVue/>
  <div class="absolute top-0 z-30 w-screen h-screen bg-black bg-opacity-90">
  </div>
  <div class="absolute top-0 z-40 w-screen h-screen ">
    <div class="h-full w-full flex justify-center items-center">
      <div class="text-white text-2xl md:text-8xl font-bold">
           PROYECTOS DE INVERSIÓN 
            <div class="flex justify-center items-center">
           {{obj.prop}}
      </div>
      </div>
     
    </div>
  </div>
  <div class="absolute top-0 z-30 w-screen h-screen ">
    <div class="flex h-full w-full justify-center items-end ">
      <div class=" flex w-full justify-between">
  <div class="w-96 m-auto animate__animated animate__fadeInUp">
      <div
    class=" grid grid-cols-3 grid-rows-7 grid-flow-row overflow-hidden rounded-lg shadow-md bg-white hover:shadow-xl transition-shadow duration-300 ease-in-out"
  >
    <div class="col-span-3 row-span-4 p-1 m-1 ">
      <a href="#">
        <img
          src="https://images.squarespace-cdn.com/content/v1/5ef22b6b4e77df552c948caa/1595438867422-H42JMMGB5HQH6ORINO36/ke17ZwdGBToddI8pDm48kJK4Mm1kch8SFO9ZNkN1NT97gQa3H78H3Y0txjaiv_0fDoOvxcdMmMKkDsyUqMSsMWxHk725yiiHCCLfrh8O1z5QHyNOqBUUEtDDsRWrJLTmFk_H6M1tkD9NpL7mXac0oVSXdFfjxR5AjcLwGSebOiGBsFzzcw3xKxvyC_6CFFG_/maguey-token.jpg?format=500w"
          alt="Placeholder"
          class="rounded-t-xl object-cover h-48 w-full"
        />
      </a>
    </div>

    <div class="col-span-3 row-span-1">
      
    </div>

    <div class="col-span-3 row-span-1">
      
    </div>
  </div>
</div>
<div class="w-96 m-auto animate__animated animate__fadeInUp">
      <div
    class=" grid grid-cols-3 grid-rows-7 grid-flow-row overflow-hidden rounded-lg shadow-md bg-white hover:shadow-xl transition-shadow duration-300 ease-in-out"
  >
    <div class="col-span-3 row-span-4 p-1 m-1 ">
      <a href="#">
        <img
          src="https://images.squarespace-cdn.com/content/v1/5ef22b6b4e77df552c948caa/1601339596671-DOBMXDDOCTZVSF8DXKS7/ke17ZwdGBToddI8pDm48kJK4Mm1kch8SFO9ZNkN1NT97gQa3H78H3Y0txjaiv_0fDoOvxcdMmMKkDsyUqMSsMWxHk725yiiHCCLfrh8O1z5QHyNOqBUUEtDDsRWrJLTmFk_H6M1tkD9NpL7mXac0oVSXdFfjxR5AjcLwGSebOiGBsFzzcw3xKxvyC_6CFFG_/mercado-bursatil.jpg?format=500w"
          alt="Placeholder"
          class="rounded-t-xl object-cover h-48 w-full"
        />
      </a>
    </div>

    <div class="col-span-3 row-span-1">
      
    </div>

    <div class="col-span-3 row-span-1">
      
    </div>
  </div>
</div>
<div class="w-96 m-auto animate__animated animate__fadeInUp">
      <div
    class=" grid grid-cols-3 grid-rows-7 grid-flow-row overflow-hidden rounded-lg shadow-md bg-white hover:shadow-xl transition-shadow duration-300 ease-in-out"
  >
    <div class="col-span-3 row-span-4 p-1 m-1 ">
      <a href="#">
        <img
          src="https://images.squarespace-cdn.com/content/v1/5ef22b6b4e77df552c948caa/1595438944917-VCE13TTH26PONLR6AH5U/ke17ZwdGBToddI8pDm48kJK4Mm1kch8SFO9ZNkN1NT97gQa3H78H3Y0txjaiv_0fDoOvxcdMmMKkDsyUqMSsMWxHk725yiiHCCLfrh8O1z5QHyNOqBUUEtDDsRWrJLTmFk_H6M1tkD9NpL7mXac0oVSXdFfjxR5AjcLwGSebOiGBsFzzcw3xKxvyC_6CFFG_/hotel-boutique-santo-domingo.jpg?format=500w"
          alt="Placeholder"
          class="rounded-t-xl object-cover h-48 w-full"
        />
      </a>
    </div>

    <div class="col-span-3 row-span-1">
      
    </div>

    <div class="col-span-3 row-span-1">
      
    </div>
  </div>
</div>
</div>
    </div>

  </div>
</template>

<script>
import headMenuComponentVue from '../components/otros/headMenuComponent.vue'
import Otro3dDemoVue from '../components/otros/Otro3dDemo.vue'
import gsap from "gsap";
export default {
  data() {
    return {
      obj:  {prop: 10},
    }
  },
  components: {
    headMenuComponentVue,
    Otro3dDemoVue
  },
  mounted () {
    
gsap.to(this.obj, {
  duration: 5,
  prop: 10000, 
  //onUpdate fires each time the tween updates; we'll explain callbacks later.
  onUpdate: function() {
    console.log(this.obj.prop); //logs the value on each update.
  }
});
  },
}
</script>

<style>

</style>