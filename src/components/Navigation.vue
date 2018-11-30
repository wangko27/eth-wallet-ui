<template>
  <aside class="navigation">
    <nav class="height-100p">
      <ul class="nav luna-nav">

        <li ng-class="{active: vm.data.currentPage == '/'}" class="active">
          <a href="/">Home</a>
        </li>

        <li ng-class="{active: vm.data.currentPage == '/peers'}">
          <a href="/peers">Ethereum Peers</a>
        </li>

        <li ng-class="{active: vm.data.currentPage == '/systemLog'}">
          <a href="/systemLog">System Logs</a>
        </li>

        <li ng-class="{active: vm.data.currentPage == '/rpcUsage'}">
          <a href="/rpcUsage">JSON-RPC Usage</a>
        </li>

        <li ng-class="{active: vm.data.currentPage == '/terminal'}" ng-show="vm.data.featureRpc" class="">
          <a href="/terminal">Terminal</a>
        </li>

        <li ng-class="{active: vm.data.currentPage == '/wallet'}">
          <a href="/wallet">Wallet</a>
        </li>

        <li ng-class="{active: vm.data.currentPage == '/contracts'}" ng-show="vm.data.featureContracts" class="">
          <a href="/contracts">Contracts</a>
        </li>

        <div class="text-center m-l-md m-r-md m-t-lg" ng-hide="!vm.data.privateNetwork">
          <h5 class="c-yellow"><i class="fa fa-gears m-r-sm"></i>Private network</h5>
          <small>Peer discovery is disabled</small>
          <br>
          <small>Mining is auto started</small>
        </div>


        <!-- INSTANT STATS -->
        <li class="nav-info instant-stats">

          <h5 class="m-t-md m-b-xs v-c">
            <i class="pe pe-7s-shield text-warning"></i>
            Harmony Health
          </h5>
          <!--pe pe-7s-global text-warning-->

          <!-- CPU -->
          <div class="m-t-xs">
            CPU usage: <span class="c-white ng-binding">29 %</span>
          </div>
          <div class="">
            <div class="progress m-t-xs full progress-small">
              <div id="cpuUsageProgress" aria-valuemax="100" aria-valuemin="0" aria-valuenow="29" role="progressbar" class="width-0p progress-bar progress-bar-warning" style="width: 29%;">
                <span class="sr-only ng-binding">29%</span>
              </div>
            </div>
          </div>

          <!-- Memory -->
          <div class="m-t-xs">
            Memory usage: <span class="c-white ng-binding">1.09 GB</span>
          </div>
          <div class="">
            <div class="progress m-t-xs full progress-small">
              <div id="memoryUsageProgress" aria-valuemax="100" aria-valuemin="0" aria-valuenow="58" role="progressbar" class="width-0p progress-bar progress-bar-warning" style="width: 58%;">
                <span class="sr-only ng-binding">1.09 GB</span>
              </div>
            </div>
          </div>

          <!-- Disk -->
          <div class="m-t-xs">
            DB size: <span class="c-white ng-binding">3.88 MB</span>
          </div>
          <div class="">
            <div class="progress m-t-xs full progress-small">
              <div id="diskUsageProgress" aria-valuemax="100" aria-valuemin="0" aria-valuenow="0" role="progressbar" class="width-0p progress-bar progress-bar-warning" style="width: 0%;">
                <span class="sr-only ng-binding">3.88 MB</span>
              </div>
            </div>
          </div>

          <div class="m-t-xl" data-toggle="tooltip" title="Hash: 561582b,   Created: [GMT]-[26/Oct/2018]-[13:04]">
            <small>
              Ethereum Harmony <span class="c-white m-l-xs ng-binding">v.2.3</span>
            </small>
            <br>
            <small>
              <small>EthereumJ <span class="c-white m-l-xs ng-binding">1.10.0-SNAPSHOT</span></small>
            </small>
          </div>

        </li>
      </ul>
    </nav>
  </aside>
</template>

<script>
    export default {
        name: "Navigation"
    }
</script>

<style scoped>

</style>
