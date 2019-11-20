<template>
<section>
  <Navbar /> 
  <div id="main">
    <div class="container f-sm-fluid"> 
      <main>
        <div>
          <nuxt />
        </div>
      </main>
    </div>
  </div>
  </section>
</template>

<script>
import Navbar from '~/components/Navbar'
export default {
  components: {
    Navbar
  }
  
}
</script>
<style>
  html{
    background: linear-gradient(0deg, rgba(221,221,221,1) 0%, rgba(235,235,235,1) 60%, rgba(255,255,255,1) 70%, rgba(235,235,235,1) 80%, rgba(221,221,221,1) 100% )!important;
    background-repeat: no-repeat!important;
    background-attachment: fixed!important;
  }
  #main{
    margin: 0 auto;

  }
  body{
    background-color: transparent;
  }
  .header-shadow{
    height: 4rem;
    background: linear-gradient(90deg, rgba(221,221,221,1) 0%, rgba(235,235,235,1) 0%, rgba(235,235,235,1) 32%, rgba(255,255,255,1) 50%, rgba(235,235,235,1) 68%, rgba(219,219,219,1) 100%);
    margin-bottom: 1rem;
    box-shadow: 0 -1px 4px 0px rgba(0, 0, 0, 0.25);
  }
  li.nav-item:hover {
    box-shadow: inset 0px -10px 10px -5px rgba(255, 255, 255, 0.78);
    transition: all .3s ease-in-out;
    filter: saturate(1.2);
}
  @media ( max-width:767px){
  .container{
    max-width: 73%;
  }
  .color-red{
    color:#c20116;
  }

  .container {
    max-width: 100%!important;
    }
}
</style>
