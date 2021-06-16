<template>
  <div>
    <threeanimationinicialVue/>
    <Principal3dComponentVue/>
    <TitlesComponetVue/>
  </div>
</template>

<script>
import Principal3dComponentVue from '../components/Principal3dComponent.vue'
import threeanimationinicialVue from '../components/threeanimationinicial.vue'
import TitlesComponetVue from '../components/TitlesComponet.vue'
export default {
  name: 'Home',
  components: {
    threeanimationinicialVue,
    Principal3dComponentVue,
    TitlesComponetVue
  }
}
</script>
