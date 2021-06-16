<template>
  <div>
    <threeanimationinicialVue/>
    <Principal3dComponentVue/>
  </div>
</template>

<script>
import Principal3dComponentVue from '../components/Principal3dComponent.vue'
import threeanimationinicialVue from '../components/threeanimationinicial.vue'
export default {
  name: 'Home',
  components: {
    threeanimationinicialVue,
    Principal3dComponentVue
  }
}
</script>
