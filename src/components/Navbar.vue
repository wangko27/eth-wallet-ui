<template>
  <nav class="navbar navbar-default navbar-fixed-top">
    <div class="container-fluid">
      <div class="navbar-header">
        <div id="mobile-menu">
          <div class="left-nav-toggle">
            <a href="/">
              <i class="stroke-hamburgermenu"></i>
            </a>
          </div>
        </div>
        <a class="navbar-brand main-logo" href="/">
          <!--<img src="images/harmony-title.svg" onerror="this.src='images/harmony-logo.png'"/>-->
          <img src="/static/images/large_EH_logo.png">
        </a>
      </div>
      <div id="navbar" class="navbar-collapse collapse">
        <div class="left-nav-toggle">
          <a href="">
            <i class="stroke-hamburgermenu"></i>
          </a>
        </div>

        <div class="topbar m-b-none" ng-show="syncStateReceived">

          <!-- ngIf: isSyncOff -->

          <!-- ngIf: isLoadingState && !isSyncOff -->

          <!-- ngIf: !isLoadingState && !isSyncComplete && !isRegularSync && !isSyncOff -->

          <div class="panel tp-panel" ng-show="!isLoadingState || isLoadingStateWithBlocks">
            <div class="panel-body" data-toggle="tooltip" title="Created at 02:46:08 Nov 30 2018">
                            <span class="m-b-none ng-binding">
                                #<span id="blockCounter" class="tp-title" value="7179">7,179</span> (a few seconds ago)
                            </span>
              <div class="top-bar-line"></div>
              <div class="small">Last Block Imported</div>
            </div>
          </div>

          <div class="panel tp-panel" ng-show="!isLoadingState || isLoadingStateWithBlocks">
            <div class="panel-body">
                            <span class="m-b-none tp-title ng-binding">
                                0
                            </span>
              <div class="top-bar-line"></div>
              <div class="small">Transactions</div>
            </div>
          </div>

          <div class="panel tp-panel" ng-show="!isLoadingState || isLoadingStateWithBlocks">
            <div class="panel-body">
                            <span class="m-b-none tp-title ng-binding">
                                302.67 kBH
                            </span>
              <div class="top-bar-line"></div>
              <div class="small">Difficulty</div>
            </div>
          </div>

          <div class="panel tp-panel" ng-show="!isLoadingState || isLoadingStateWithBlocks">
            <div class="panel-body">
                            <span class="m-b-none tp-title ng-binding">
                                1 GWei
                            </span>
              <div class="top-bar-line"></div>
              <div class="small">Recommended Gas Price</div>
            </div>
          </div>

          <div class="panel tp-panel" ng-show="!isLoadingState || isLoadingStateWithBlocks">
            <div class="panel-body">
                            <span class="m-b-none tp-title ng-binding">
                                33  H/s
                            </span>
              <div class="top-bar-line"></div>
              <div class="small">Avg Hash Rate</div>
            </div>
          </div>

        </div>

      </div>
    </div>
  </nav>
</template>

<script>
  export default {
    name: "Navbar"
  }
</script>

<style scoped>

</style>
