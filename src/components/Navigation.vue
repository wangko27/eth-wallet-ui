<template>
  <aside class="navigation">
    <nav class="height-100p">
      <ul class="nav luna-nav">

        <router-link tag="li" to="/latest" active-class="active">
          <a href="/">Home</a>
        </router-link>

        <router-link tag="li" to="/peers" active-class="active">
          <a href="/peers">Ethereum Peers</a>
        </router-link>

        <router-link tag="li" to="/logs" active-class="active">
          <a href="/systemLog">System Logs</a>
        </router-link>

        <router-link tag="li" to="/rpcUsage" active-class="active">
          <a href="/rpcUsage">JSON-RPC Usage</a>
        </router-link>

        <router-link tag="li" to="/terminal" active-class="active">
          <a href="/terminal">Terminal</a>
        </router-link>

        <router-link tag="li" to="/wallet" active-class="active">
          <a href="/wallet">Wallet</a>
        </router-link>

        <router-link tag="li" to="/contracts" active-class="active">
          <a href="/contracts">Contracts</a>
        </router-link>

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
              <div id="cpuUsageProgress" aria-valuemax="100" aria-valuemin="0" aria-valuenow="29" role="progressbar"
                   class="width-0p progress-bar progress-bar-warning" style="width: 29%;">
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
              <div id="memoryUsageProgress" aria-valuemax="100" aria-valuemin="0" aria-valuenow="58" role="progressbar"
                   class="width-0p progress-bar progress-bar-warning" style="width: 58%;">
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
              <div id="diskUsageProgress" aria-valuemax="100" aria-valuemin="0" aria-valuenow="0" role="progressbar"
                   class="width-0p progress-bar progress-bar-warning" style="width: 0%;">
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
