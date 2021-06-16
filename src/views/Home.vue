<template>
  <div>
    <threeanimationinicialVue/>
    <Principal3dComponentVue/>
    <TitlesComponetVue/>
  <CardComponentVue/>
  <ContrucComponentVue/>
  <div class="h-40"></div>  
  <TeamCardsVue/>
  </div>
</template>

<script>
import CardComponentVue from '../components/CardComponent.vue'
import ContrucComponentVue from '../components/ContrucComponent.vue'
import Principal3dComponentVue from '../components/Principal3dComponent.vue'
import TeamCardsVue from '../components/TeamCards.vue'
import threeanimationinicialVue from '../components/threeanimationinicial.vue'
import TitlesComponetVue from '../components/TitlesComponet.vue'
export default {
  name: 'Home',
  components: {
    threeanimationinicialVue,
    Principal3dComponentVue,
    CardComponentVue ,
    TitlesComponetVue,
    ContrucComponentVue,
    TeamCardsVue,
  }
}
</script>
