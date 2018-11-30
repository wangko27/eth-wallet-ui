<template>
  <div class="container-fluid">
    <div class="row">
      <div class="col-lg-12">
        <div class="view-header">
          <div class="pull-right text-right text-14">
            <small>Ethereum Harmony<br>Dashboard<br> <span class="c-white ng-binding">v.2.3</span></small>
          </div>
          <div class="header-icon">
            <i class="pe page-header-icon pe-7s-graph3"></i>
          </div>
          <div class="header-title">
            <h3 class="m-b-xs">Ethereum Harmony</h3>
            <small>
              Showing recent blockchain blocks
            </small>
          </div>
        </div>
        <hr>
      </div>
    </div>
    <div class="row">
      <div class="col-lg-6">
        <!--home info-->
        <Info></Info>
        <!--home info end-->

        <!--top block miners-->
        <Top></Top>
        <!--top block miners end-->
      </div>
      <div class="col-lg-6 height-100p">
      </div>
    </div>
  </div>
</template>

<script>
  import Info from '@/components/home/Info'
  import Top from '@/components/home/Top'
  export default {
    name: "Dashboard",
    components: {Info, Top},
  }
</script>

<style scoped>

</style>
