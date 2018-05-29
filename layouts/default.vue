<template>
  <div>
    <section>
      <Navbar></Navbar>
      <nuxt/>
      <Footer></Footer>
    </section>
  </div>
</template>

<script>
  import Navbar from '../components/Navbar'
  import Footer from '../components/Footer'

  export default {
    components: {
      Navbar,
      Footer
    }
  }
</script>

<style>
  html {
    font-family: "Source Sans Pro", "Helvetica Neue", Arial, sans-serif;
    color: #555;
  }
  #full {
    height: 100%;
  }
  html,body{
    padding: 0px;
    height: 100%;
    padding: 0px;
  }
  .page-enter-active,
  .page-leave-active {
    opacity: 1;
    transition: opacity .25s;
    animation-duration: .3s;
    animation-fill-mode: both;
  }

  .page-enter-active {
    animation-name: pageFadeInUp;
  }

  .page-leave-active {
    animation-name: pageFadeOutDown;
  }

  .page-enter, .page-leave-to {
    opacity: 0;
  }


  @keyframes pageFadeInUp {
    0% {
      opacity: 0;
      transform: translate3d(0, 1.25%, 0);
    }

    to {
      opacity: 1;
      transform: none;
    }
  }

  @keyframes pageFadeOutDown {
    0% {
      opacity: 1;
    }

    to {
      opacity: 0;
      transform: translate3d(0, 1.25%, 0);
  }
}
</style>