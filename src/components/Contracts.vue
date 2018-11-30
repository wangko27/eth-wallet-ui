<template>
  <div class="container-fluid">

    <div class="row height-100p">
      <div class="col-lg-12">
        <div class="view-header">
          <div class="header-icon">
            <i class="pe page-header-icon pe-7s-albums"></i>
          </div>

          <div class="header-title">
            <div class="pull-right">
              <p ng-show="syncedBlock == 1" class="">Index is full. We can show all properties</p>
              <p ng-show="syncedBlock == -1" class="ng-hide">Index is not ready</p>
              <p ng-show="syncedBlock > 1" class="ng-hide">Contracts, added since block <b
                class="c-white ng-binding">#1</b>, will be displayed correctly</p>
              <p>Storage used for index <b class="c-white ng-binding">829 B</b> | Solc version <b
                class="c-white ng-binding">0.4.19</b></p>
            </div>

            <h3 class="m-b-xs">Contracts</h3>
            <small>
              Watch contracts' storage fields
            </small>
          </div>
          <hr>
        </div>
      </div>
    </div>

    <div class="row height-100p">

      <div class="col-lg-12 height-100p">

        <!-- ngIf: isViewingStorage -->


        <!-- ngIf: !isAddingContract && !isViewingStorage && !isDisabled -->
        <div class="panel panel-filled ng-scope"
             ng-if="!isAddingContract &amp;&amp; !isViewingStorage &amp;&amp; !isDisabled">

          <div class="panel-heading">

            <a href="#" ng-click="onWatchContract()" class="btn btn-w-md btn-primary">
              <i class="fa fa-eye m-r-sm"></i>
              Add contract for watching
            </a>
          </div>

          <div class="panel-body mCustomScrollbar _mCS_2 mCS-autoHide mCS_no_scrollbar" id="contracts-scroll-container"
               style="height: 621px;">
            <div id="mCSB_2" class="mCustomScrollBox mCS-dark mCSB_vertical mCSB_inside" tabindex="0"
                 style="max-height: none;">
              <div id="mCSB_2_container" class="mCSB_container mCS_y_hidden mCS_no_scrollbar_y"
                   style="position:relative; top:0; left:0;" dir="ltr">

                <div class="table-responsive">
                  <table class="table peers-table">
                    <thead>
                    <tr>
                      <th>
                        Contract Name
                      </th>
                      <th>
                        Address
                      </th>
                      <th>
                      </th>
                      <th>
                      </th>
                    </tr>
                    </thead>
                    <tbody>

                    <!-- ngRepeat: item in contracts -->

                    </tbody>
                  </table>
                </div>
              </div>
              <div id="mCSB_2_scrollbar_vertical"
                   class="mCSB_scrollTools mCSB_2_scrollbar mCS-dark mCSB_scrollTools_vertical" style="display: none;">
                <div class="mCSB_draggerContainer">
                  <div id="mCSB_2_dragger_vertical" class="mCSB_dragger"
                       style="position: absolute; min-height: 30px; height: 0px; top: 0px;">
                    <div class="mCSB_dragger_bar" style="line-height: 30px;"></div>
                  </div>
                  <div class="mCSB_draggerRail"></div>
                </div>
              </div>
            </div>
          </div>
        </div><!-- end ngIf: !isAddingContract && !isViewingStorage && !isDisabled -->
        <!-- ngIf: isDisabled -->
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    name: "Contracts"
  }
</script>

<style scoped>

</style>
