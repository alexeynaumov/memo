<template>
<div>
  <div class="row">
    Some content
  </div>
  <div class="row">
    <carousel style="width: 60%" /> 
  </div>
</div>

</template>

<style>
</style>

<script>
import Carousel from '../components/Carousel.vue'

export default {
  name: 'PageIndex',
  components: {
    Carousel
  }  
}
</script>
