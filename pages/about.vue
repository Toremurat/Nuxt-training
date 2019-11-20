<template>
<div>
  <div id="app">
    <carousel></carousel>
  </div>
</div>
</template>
<script>
import carousel from '~/components/Carousel'
import { VueperSlides, VueperSlide } from 'vueperslides'
// Since v. 1.6.0, you need to include Vueper Slides CSS file for default styles.
import 'vueperslides/dist/vueperslides.css'
export default {
  components:{
  carousel
}
}
</script>
<style scoped>

body{
  background-color: #000;
}
.carousel{
  margin-top: 50px;
}
.carousel-inner{
  height: 100px;
}
.carousel-caption{
  color: #fff;
  top: 50%;
}

</style>