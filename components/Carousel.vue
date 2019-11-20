<template>
  <div class="container">
  <div class='carousel-view'>
    <transition-group
      class='carousel'
      tag="div">
      <div
        v-for="slide in slides" 
        class='slide'
        :key="slide.id">
        <p>
          <span> Client: №{{ slide.id }} </span><br />
          <span> From: {{ slide.name }} </span><br />
          <span>Email: {{ slide.email }} </span><br />
          <span>City: {{ slide.address.city }} </span><br />
          <span>Message: {{ slide.company.catchPhrase }} </span><br />
          <span> {{ slide.company.bs }} </span>
        </p>
      </div>
    </transition-group>
    </div>
    <b-row>
      <b-col lg="6" md="6" cols="6"><a href="#" class="arrow-button lf" @click="previous"><fa :icon="['fas', 'angle-left']" /></a></b-col>    
      <b-col lg="6" md="6" cols="6"><a href="#" class="arrow-button rt" @click="next"><fa :icon="['fas', 'angle-right']" /></a></b-col>
    </b-row>
    </div>
</template>
<script>
export default {
  data () {
    return {
      slides: []
    }
  },
  //   async asyncData({$axios}){
  //   const slides = await $axios.$get('https://jsonplaceholder.typicode.com/users')
  //   return {slides}
  // },
  async mounted() {
    this.slides = await this.$axios.$get('https://jsonplaceholder.typicode.com/users')
  },
  methods: {
    next () {
      const first = this.slides.shift()
      this.slides = this.slides.concat(first)
    },
    previous () {
      const last = this.slides.pop()
      this.slides = [last].concat(this.slides)
    }
  }
}
</script>
<style lang="scss" scoped>
.carousel-view {
  display: flex;
  flex-direction: column;
  align-items: center;
}
.carousel {
  display: flex;
  justify-content: center;
  align-items: center;
  overflow: hidden;
  
  width: 65em;
  min-height: 25em;
}
.slide {
  flex: 0 0 30em;
  height: 20em;
  margin: 1em;
  padding: 25px 30px;
  justify-content: space-around;
  display: flex;
  align-items: center;
  border: 0.1em dashed #000;
  border-radius: 12px;
  transition: transform 0.3s ease-in-out;
}
.slide:first-of-type {
  opacity: 0;
}
.slide:last-of-type {
  opacity: 0;
}

a.arrow-button {
  margin: 1em auto;
  width: 280px;
  text-align: center;
  background: -webkit-gradient(linear, left bottom, left top, from(#dddddd), color-stop(0%, #d9d9d9), color-stop(69%, #e9e9e9), color-stop(100%, white), color-stop(100%, #ebebeb), to(#dbdbdb));
    background: linear-gradient(0deg, #dddddd 0%, #d9d9d9 0%, #e9e9e9 69%, white 100%, #ebebeb 100%, #dbdbdb 100%);
    box-shadow: 0px 2px 3px 1px rgba(0, 0, 0, 0.2);
  padding: 0.5em 0;
  display: block;
  color: rgba(0, 0, 0, 0.4);
  text-decoration: none;
  text-transform: uppercase;
  transition: all 0.2s;
  border-radius: 8px;
  &:hover {
    color: #eee;
    background-color: #333;
  }
}
@media (min-width:769px){
a.arrow-button.rt {
    position: relative;
    right: -28%;
    top: -30%;
    width: 30%;
    height: 3rem;
    line-height: 3.2rem;
    font-size: 3em;
    padding: 0;
}
a.arrow-button.lf {
    position: relative;
    right: 27%;
    top: -30%;
    width: 30%;
    height: 3rem;
    line-height: 3.2rem;
    font-size: 3em;
    padding: 0;
}
}
@media (max-width:767px){
// .slide:nth-child(6n) {
//     margin-right: 33rem!important;
//     flex: 0 0 26em!important;
// }
a.arrow-button.rt {
    position: absolute;
    right: 1%;
    bottom: 38.2%;
    width: 2em;
    height: 2em;
    line-height: 0rem;
    font-size: 1.5em;
}
a.arrow-button.lf {
    position: absolute;
    left: 1%;
    bottom: 38.2%;
    width: 2em;
    height: 2em;
    line-height: 0rem;
    font-size: 1.5em;
}
  .container {
    max-width: 100%!important;
    }
  .d-sm-none{
    display: none;
}

}
</style>