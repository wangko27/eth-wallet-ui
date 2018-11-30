<template>
  <div id="app" class="wrapper">
    <!-- Header-->
    <Navbar></Navbar>
    <!-- End header-->

    <!-- NAVIGATION-->
    <Navigation></Navigation>
    <!-- End NAVIGATION-->

    <!-- MAIN CONTENT AND INJECTED VIEWS -->
    <div id="main">
      <section class="content">
        <router-view></router-view>
      </section>
    </div>
  </div>
</template>

<script>
  import Navbar from '@/components/Navbar'
  import Navigation from '@/components/Navigation'

  export default {
    name: 'App',
    components: {Navbar, Navigation},
  }
</script>
