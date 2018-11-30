<template>
  <div id="app" class="wrapper">
    <!-- Header-->
    <Navbar></Navbar>
    <!-- End header-->

    <!-- NAVIGATION-->
    <Navigation></Navigation>
    <!-- End NAVIGATION-->

    <!-- MAIN CONTENT AND INJECTED VIEWS -->
    <Dashboard></Dashboard>
  </div>
</template>

<script>
  import Navbar from '@/components/Navbar'
  import Navigation from '@/components/Navigation'
  import Dashboard from '@/components/Dashboard'

  export default {
    name: 'App',
    components: {Navbar, Navigation, Dashboard},
  }
</script>
