<template>
  <div id="main">
    <!-- angular templating -->
    <!-- this is where content will be injected -->
    <!-- ngView: -->
    <div ng-view="" class="ng-scope">
    <!-- Main content-->
    <section class="content ng-scope">
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
            <!--home info end-->

            <!--top block miners-->
            <!--top block miners end-->
          </div>

          <div class="col-lg-6 height-100p">

          </div>
        </div>

      </div>
    </section>
    <!-- End main content--></div>

  </div>
</template>

<script>
    export default {
        name: "Dashboard"
    }
</script>

<style scoped>

</style>
