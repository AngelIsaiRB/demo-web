<template>
  <div>
    <threeanimationinicialVue/>
    <Principal3dComponentVue/>
    <TitlesComponetVue/>
  <CardComponentVue/>
  <ContrucComponentVue/>
  
  </div>
</template>

<script>
import CardComponentVue from '../components/CardComponent.vue'
import ContrucComponentVue from '../components/ContrucComponent.vue'
import Principal3dComponentVue from '../components/Principal3dComponent.vue'
import threeanimationinicialVue from '../components/threeanimationinicial.vue'
import TitlesComponetVue from '../components/TitlesComponet.vue'
export default {
  name: 'Home',
  components: {
    threeanimationinicialVue,
    Principal3dComponentVue,
    CardComponentVue ,
    TitlesComponetVue,
    ContrucComponentVue
  }
}
</script>
