<template>
  <div class="container-fluid">
    <div class="row">
      <div class="col-lg-12">
        <div class="view-header">

          <div class="m-l-sm pull-right text-right rpc-filter-div">
            <form class="navbar-form navbar-right ng-pristine ng-valid" role="search">
              <div class="form-group">
                <input type="text" class="form-control query ng-pristine ng-valid ng-empty ng-touched"
                       placeholder="Filter by name" tabindex="1" ng-model="filterWord">
              </div>
            </form>
          </div>

          <div class="header-icon">
            <i class="pe page-header-icon pe-7s-graph3"></i>
          </div>

          <div class="header-title">
            <h3 class="m-b-xs">Json-Rpc API Usage</h3>
            <small>
              Displaying JSON-RPC protocol tracing.
            </small>
          </div>

        </div>

        <hr>
      </div>
    </div>
    <div class="table-responsive mCustomScrollbar _mCS_3 mCS-autoHide" id="rpc-scroll-container" style="height: 675px;">
      <div id="mCSB_3" class="mCustomScrollBox mCS-dark mCSB_vertical mCSB_inside" tabindex="0"
           style="max-height: none;">
        <div id="mCSB_3_container" class="mCSB_container" style="position: relative; top: 0px; left: 0px;" dir="ltr">
          <ul class="table peers-table">

            <!-- ngRepeat: item in rpcItems | rpcItemFilter:filterWord -->
            <il ng-repeat="item in rpcItems | rpcItemFilter:filterWord" class="ng-scope">
              <div class="panel panel-dark-filled">
                <div class="panel-heading p-b-none p-t-none">
                  <div class="row">
                    <div class="col-sm-6">
                      <u><h4 class="font-weight-normal ng-binding">admin_addPeer</h4></u>
                    </div>
                    <div class="col-sm-3">
                      <h5 class="font-weight-normal ng-binding ng-hide" ng-show="item.count > 0">Invoked: 0</h5>
                    </div>
                    <div class="col-sm-3 m-l-none">
                      <h5 class="font-weight-normal ng-binding ng-hide" ng-show="item.lastTime">Last call: </h5>
                    </div>
                  </div>
                </div>

                <div class="panel-footer p-b-none p-t-none">
                  <!-- Last Result -->
                  <div class="rpc-item-header ng-hide" ng-show="item.lastResult != null">
                    <a href="#" ng-click="showLastResult(item)">
                      <div class="header-icon m-r-md" style="margin-right: 8px;">
                        <i class="pe page-header-icon pe-7s-plus"></i>
                      </div>
                      <div class="header-title m-l-md"><h5 class="rpc-item-text">Last Result</h5>
                      </div>
                    </a>
                  </div>

                  <div class="rpc-item-result-admin_addPeer ng-hide"
                       ng-show="item.lastResult != null &amp;&amp; item.isLastResultVisible">
                    <pre class="panel panel-black-filled rpc-item-result ng-binding">null</pre>
                  </div>

                  <!-- Usage Sample -->
                  <div class="rpc-item-header flex-row flex-align-center rpc-usage">
                    <!--<a href="#" ng-click="showUsageHelp(item.methodName)">-->
                    <div class="header-icon m-l-none m-r-xs">
                      <i class="pe page-header-icon pe-7s-study"></i>
                    </div>
                    <pre class="panel panel-black-filled m-t-xs m-b-xs ng-binding">curl -X POST --data '{"jsonrpc":"2.0","method":"admin_addPeer","params":["0x0"],"id":64}' <span
                      class="ng-binding">http://localhost:8080/rpc</span></pre>
                    <!--<div class="header-title"><h5 class="rpc-item-text">Curl</h5>-->
                    <!--</div>-->
                    <!--</a>-->

                  </div>
                </div>
              </div>
            </il><!-- end ngRepeat: item in rpcItems | rpcItemFilter:filterWord -->
            <il ng-repeat="item in rpcItems | rpcItemFilter:filterWord" class="ng-scope">
              <div class="panel panel-dark-filled">
                <div class="panel-heading p-b-none p-t-none">
                  <div class="row">
                    <div class="col-sm-6">
                      <u><h4 class="font-weight-normal ng-binding">admin_nodeInfo</h4></u>
                    </div>
                    <div class="col-sm-3">
                      <h5 class="font-weight-normal ng-binding ng-hide" ng-show="item.count > 0">Invoked: 0</h5>
                    </div>
                    <div class="col-sm-3 m-l-none">
                      <h5 class="font-weight-normal ng-binding ng-hide" ng-show="item.lastTime">Last call: </h5>
                    </div>
                  </div>
                </div>

                <div class="panel-footer p-b-none p-t-none">
                  <!-- Last Result -->
                  <div class="rpc-item-header ng-hide" ng-show="item.lastResult != null">
                    <a href="#" ng-click="showLastResult(item)">
                      <div class="header-icon m-r-md" style="margin-right: 8px;">
                        <i class="pe page-header-icon pe-7s-plus"></i>
                      </div>
                      <div class="header-title m-l-md"><h5 class="rpc-item-text">Last Result</h5>
                      </div>
                    </a>
                  </div>

                  <div class="rpc-item-result-admin_nodeInfo ng-hide"
                       ng-show="item.lastResult != null &amp;&amp; item.isLastResultVisible">
                    <pre class="panel panel-black-filled rpc-item-result ng-binding">null</pre>
                  </div>

                  <!-- Usage Sample -->
                  <div class="rpc-item-header flex-row flex-align-center rpc-usage">
                    <!--<a href="#" ng-click="showUsageHelp(item.methodName)">-->
                    <div class="header-icon m-l-none m-r-xs">
                      <i class="pe page-header-icon pe-7s-study"></i>
                    </div>
                    <pre class="panel panel-black-filled m-t-xs m-b-xs ng-binding">curl -X POST --data '{"jsonrpc":"2.0","method":"admin_nodeInfo","params":[],"id":64}' <span
                      class="ng-binding">http://localhost:8080/rpc</span></pre>
                    <!--<div class="header-title"><h5 class="rpc-item-text">Curl</h5>-->
                    <!--</div>-->
                    <!--</a>-->

                  </div>
                </div>
              </div>
            </il><!-- end ngRepeat: item in rpcItems | rpcItemFilter:filterWord -->
            <il ng-repeat="item in rpcItems | rpcItemFilter:filterWord" class="ng-scope">
              <div class="panel panel-dark-filled">
                <div class="panel-heading p-b-none p-t-none">
                  <div class="row">
                    <div class="col-sm-6">
                      <u><h4 class="font-weight-normal ng-binding">admin_peers</h4></u>
                    </div>
                    <div class="col-sm-3">
                      <h5 class="font-weight-normal ng-binding ng-hide" ng-show="item.count > 0">Invoked: 0</h5>
                    </div>
                    <div class="col-sm-3 m-l-none">
                      <h5 class="font-weight-normal ng-binding ng-hide" ng-show="item.lastTime">Last call: </h5>
                    </div>
                  </div>
                </div>

                <div class="panel-footer p-b-none p-t-none">
                  <!-- Last Result -->
                  <div class="rpc-item-header ng-hide" ng-show="item.lastResult != null">
                    <a href="#" ng-click="showLastResult(item)">
                      <div class="header-icon m-r-md" style="margin-right: 8px;">
                        <i class="pe page-header-icon pe-7s-plus"></i>
                      </div>
                      <div class="header-title m-l-md"><h5 class="rpc-item-text">Last Result</h5>
                      </div>
                    </a>
                  </div>

                  <div class="rpc-item-result-admin_peers ng-hide"
                       ng-show="item.lastResult != null &amp;&amp; item.isLastResultVisible">
                    <pre class="panel panel-black-filled rpc-item-result ng-binding">null</pre>
                  </div>

                  <!-- Usage Sample -->
                  <div class="rpc-item-header flex-row flex-align-center rpc-usage">
                    <!--<a href="#" ng-click="showUsageHelp(item.methodName)">-->
                    <div class="header-icon m-l-none m-r-xs">
                      <i class="pe page-header-icon pe-7s-study"></i>
                    </div>
                    <pre class="panel panel-black-filled m-t-xs m-b-xs ng-binding">curl -X POST --data '{"jsonrpc":"2.0","method":"admin_peers","params":[],"id":64}' <span
                      class="ng-binding">http://localhost:8080/rpc</span></pre>
                    <!--<div class="header-title"><h5 class="rpc-item-text">Curl</h5>-->
                    <!--</div>-->
                    <!--</a>-->

                  </div>
                </div>
              </div>
            </il><!-- end ngRepeat: item in rpcItems | rpcItemFilter:filterWord -->
            <il ng-repeat="item in rpcItems | rpcItemFilter:filterWord" class="ng-scope">
              <div class="panel panel-dark-filled">
                <div class="panel-heading p-b-none p-t-none">
                  <div class="row">
                    <div class="col-sm-6">
                      <u><h4 class="font-weight-normal ng-binding">eth_accounts</h4></u>
                    </div>
                    <div class="col-sm-3">
                      <h5 class="font-weight-normal ng-binding ng-hide" ng-show="item.count > 0">Invoked: 0</h5>
                    </div>
                    <div class="col-sm-3 m-l-none">
                      <h5 class="font-weight-normal ng-binding ng-hide" ng-show="item.lastTime">Last call: </h5>
                    </div>
                  </div>
                </div>

                <div class="panel-footer p-b-none p-t-none">
                  <!-- Last Result -->
                  <div class="rpc-item-header ng-hide" ng-show="item.lastResult != null">
                    <a href="#" ng-click="showLastResult(item)">
                      <div class="header-icon m-r-md" style="margin-right: 8px;">
                        <i class="pe page-header-icon pe-7s-plus"></i>
                      </div>
                      <div class="header-title m-l-md"><h5 class="rpc-item-text">Last Result</h5>
                      </div>
                    </a>
                  </div>

                  <div class="rpc-item-result-eth_accounts ng-hide"
                       ng-show="item.lastResult != null &amp;&amp; item.isLastResultVisible">
                    <pre class="panel panel-black-filled rpc-item-result ng-binding">null</pre>
                  </div>

                  <!-- Usage Sample -->
                  <div class="rpc-item-header flex-row flex-align-center rpc-usage">
                    <!--<a href="#" ng-click="showUsageHelp(item.methodName)">-->
                    <div class="header-icon m-l-none m-r-xs">
                      <i class="pe page-header-icon pe-7s-study"></i>
                    </div>
                    <pre class="panel panel-black-filled m-t-xs m-b-xs ng-binding">curl -X POST --data '{"jsonrpc":"2.0","method":"eth_accounts","params":[],"id":1}' <span
                      class="ng-binding">http://localhost:8080/rpc</span></pre>
                    <!--<div class="header-title"><h5 class="rpc-item-text">Curl</h5>-->
                    <!--</div>-->
                    <!--</a>-->

                  </div>
                </div>
              </div>
            </il><!-- end ngRepeat: item in rpcItems | rpcItemFilter:filterWord -->
            <il ng-repeat="item in rpcItems | rpcItemFilter:filterWord" class="ng-scope">
              <div class="panel panel-dark-filled">
                <div class="panel-heading p-b-none p-t-none">
                  <div class="row">
                    <div class="col-sm-6">
                      <u><h4 class="font-weight-normal ng-binding">eth_blockNumber</h4></u>
                    </div>
                    <div class="col-sm-3">
                      <h5 class="font-weight-normal ng-binding ng-hide" ng-show="item.count > 0">Invoked: 0</h5>
                    </div>
                    <div class="col-sm-3 m-l-none">
                      <h5 class="font-weight-normal ng-binding ng-hide" ng-show="item.lastTime">Last call: </h5>
                    </div>
                  </div>
                </div>

                <div class="panel-footer p-b-none p-t-none">
                  <!-- Last Result -->
                  <div class="rpc-item-header ng-hide" ng-show="item.lastResult != null">
                    <a href="#" ng-click="showLastResult(item)">
                      <div class="header-icon m-r-md" style="margin-right: 8px;">
                        <i class="pe page-header-icon pe-7s-plus"></i>
                      </div>
                      <div class="header-title m-l-md"><h5 class="rpc-item-text">Last Result</h5>
                      </div>
                    </a>
                  </div>

                  <div class="rpc-item-result-eth_blockNumber ng-hide"
                       ng-show="item.lastResult != null &amp;&amp; item.isLastResultVisible">
                    <pre class="panel panel-black-filled rpc-item-result ng-binding">null</pre>
                  </div>

                  <!-- Usage Sample -->
                  <div class="rpc-item-header flex-row flex-align-center rpc-usage">
                    <!--<a href="#" ng-click="showUsageHelp(item.methodName)">-->
                    <div class="header-icon m-l-none m-r-xs">
                      <i class="pe page-header-icon pe-7s-study"></i>
                    </div>
                    <pre class="panel panel-black-filled m-t-xs m-b-xs ng-binding">curl -X POST --data '{"jsonrpc":"2.0","method":"eth_blockNumber","params":[],"id":83}' <span
                      class="ng-binding">http://localhost:8080/rpc</span></pre>
                    <!--<div class="header-title"><h5 class="rpc-item-text">Curl</h5>-->
                    <!--</div>-->
                    <!--</a>-->

                  </div>
                </div>
              </div>
            </il><!-- end ngRepeat: item in rpcItems | rpcItemFilter:filterWord -->
            <il ng-repeat="item in rpcItems | rpcItemFilter:filterWord" class="ng-scope">
              <div class="panel panel-dark-filled">
                <div class="panel-heading p-b-none p-t-none">
                  <div class="row">
                    <div class="col-sm-6">
                      <u><h4 class="font-weight-normal ng-binding">eth_call</h4></u>
                    </div>
                    <div class="col-sm-3">
                      <h5 class="font-weight-normal ng-binding ng-hide" ng-show="item.count > 0">Invoked: 0</h5>
                    </div>
                    <div class="col-sm-3 m-l-none">
                      <h5 class="font-weight-normal ng-binding ng-hide" ng-show="item.lastTime">Last call: </h5>
                    </div>
                  </div>
                </div>

                <div class="panel-footer p-b-none p-t-none">
                  <!-- Last Result -->
                  <div class="rpc-item-header ng-hide" ng-show="item.lastResult != null">
                    <a href="#" ng-click="showLastResult(item)">
                      <div class="header-icon m-r-md" style="margin-right: 8px;">
                        <i class="pe page-header-icon pe-7s-plus"></i>
                      </div>
                      <div class="header-title m-l-md"><h5 class="rpc-item-text">Last Result</h5>
                      </div>
                    </a>
                  </div>

                  <div class="rpc-item-result-eth_call ng-hide"
                       ng-show="item.lastResult != null &amp;&amp; item.isLastResultVisible">
                    <pre class="panel panel-black-filled rpc-item-result ng-binding">null</pre>
                  </div>

                  <!-- Usage Sample -->
                  <div class="rpc-item-header flex-row flex-align-center rpc-usage">
                    <!--<a href="#" ng-click="showUsageHelp(item.methodName)">-->
                    <div class="header-icon m-l-none m-r-xs">
                      <i class="pe page-header-icon pe-7s-study"></i>
                    </div>
                    <pre class="panel panel-black-filled m-t-xs m-b-xs ng-binding">curl -X POST --data '{"jsonrpc":"2.0","method":"eth_call","params":[{"from":"0xcd2a3d9f938e13cd947ec05abc7fe734df8dd826", "to":"0x79b08ad8787060333663d19704909ee7b1903e58", "gas":"0x300000", "gasPrice":"0x10000000000", "value":"0x7777", "data":"0x", "nounce":"0x101F15"}, "0x0"],"id":1}' <span
                      class="ng-binding">http://localhost:8080/rpc</span></pre>
                    <!--<div class="header-title"><h5 class="rpc-item-text">Curl</h5>-->
                    <!--</div>-->
                    <!--</a>-->

                  </div>
                </div>
              </div>
            </il><!-- end ngRepeat: item in rpcItems | rpcItemFilter:filterWord -->
            <il ng-repeat="item in rpcItems | rpcItemFilter:filterWord" class="ng-scope">
              <div class="panel panel-dark-filled">
                <div class="panel-heading p-b-none p-t-none">
                  <div class="row">
                    <div class="col-sm-6">
                      <u><h4 class="font-weight-normal ng-binding">eth_coinbase</h4></u>
                    </div>
                    <div class="col-sm-3">
                      <h5 class="font-weight-normal ng-binding ng-hide" ng-show="item.count > 0">Invoked: 0</h5>
                    </div>
                    <div class="col-sm-3 m-l-none">
                      <h5 class="font-weight-normal ng-binding ng-hide" ng-show="item.lastTime">Last call: </h5>
                    </div>
                  </div>
                </div>

                <div class="panel-footer p-b-none p-t-none">
                  <!-- Last Result -->
                  <div class="rpc-item-header ng-hide" ng-show="item.lastResult != null">
                    <a href="#" ng-click="showLastResult(item)">
                      <div class="header-icon m-r-md" style="margin-right: 8px;">
                        <i class="pe page-header-icon pe-7s-plus"></i>
                      </div>
                      <div class="header-title m-l-md"><h5 class="rpc-item-text">Last Result</h5>
                      </div>
                    </a>
                  </div>

                  <div class="rpc-item-result-eth_coinbase ng-hide"
                       ng-show="item.lastResult != null &amp;&amp; item.isLastResultVisible">
                    <pre class="panel panel-black-filled rpc-item-result ng-binding">null</pre>
                  </div>

                  <!-- Usage Sample -->
                  <div class="rpc-item-header flex-row flex-align-center rpc-usage">
                    <!--<a href="#" ng-click="showUsageHelp(item.methodName)">-->
                    <div class="header-icon m-l-none m-r-xs">
                      <i class="pe page-header-icon pe-7s-study"></i>
                    </div>
                    <pre class="panel panel-black-filled m-t-xs m-b-xs ng-binding">curl -X POST --data '{"jsonrpc":"2.0","method":"eth_coinbase","params":[],"id":64}' <span
                      class="ng-binding">http://localhost:8080/rpc</span></pre>
                    <!--<div class="header-title"><h5 class="rpc-item-text">Curl</h5>-->
                    <!--</div>-->
                    <!--</a>-->

                  </div>
                </div>
              </div>
            </il><!-- end ngRepeat: item in rpcItems | rpcItemFilter:filterWord -->
            <il ng-repeat="item in rpcItems | rpcItemFilter:filterWord" class="ng-scope">
              <div class="panel panel-dark-filled">
                <div class="panel-heading p-b-none p-t-none">
                  <div class="row">
                    <div class="col-sm-6">
                      <u><h4 class="font-weight-normal ng-binding">eth_compileLLL</h4></u>
                    </div>
                    <div class="col-sm-3">
                      <h5 class="font-weight-normal ng-binding ng-hide" ng-show="item.count > 0">Invoked: 0</h5>
                    </div>
                    <div class="col-sm-3 m-l-none">
                      <h5 class="font-weight-normal ng-binding ng-hide" ng-show="item.lastTime">Last call: </h5>
                    </div>
                  </div>
                </div>

                <div class="panel-footer p-b-none p-t-none">
                  <!-- Last Result -->
                  <div class="rpc-item-header ng-hide" ng-show="item.lastResult != null">
                    <a href="#" ng-click="showLastResult(item)">
                      <div class="header-icon m-r-md" style="margin-right: 8px;">
                        <i class="pe page-header-icon pe-7s-plus"></i>
                      </div>
                      <div class="header-title m-l-md"><h5 class="rpc-item-text">Last Result</h5>
                      </div>
                    </a>
                  </div>

                  <div class="rpc-item-result-eth_compileLLL ng-hide"
                       ng-show="item.lastResult != null &amp;&amp; item.isLastResultVisible">
                    <pre class="panel panel-black-filled rpc-item-result ng-binding">null</pre>
                  </div>

                  <!-- Usage Sample -->
                  <div class="rpc-item-header flex-row flex-align-center rpc-usage">
                    <!--<a href="#" ng-click="showUsageHelp(item.methodName)">-->
                    <div class="header-icon m-l-none m-r-xs">
                      <i class="pe page-header-icon pe-7s-study"></i>
                    </div>
                    <pre class="panel panel-black-filled m-t-xs m-b-xs ng-binding">curl -X POST --data '{"jsonrpc":"2.0","method":"eth_compileLLL","params":["(returnlll (suicide (caller)))"],"id":1}' <span
                      class="ng-binding">http://localhost:8080/rpc</span></pre>
                    <!--<div class="header-title"><h5 class="rpc-item-text">Curl</h5>-->
                    <!--</div>-->
                    <!--</a>-->

                  </div>
                </div>
              </div>
            </il><!-- end ngRepeat: item in rpcItems | rpcItemFilter:filterWord -->
            <il ng-repeat="item in rpcItems | rpcItemFilter:filterWord" class="ng-scope">
              <div class="panel panel-dark-filled">
                <div class="panel-heading p-b-none p-t-none">
                  <div class="row">
                    <div class="col-sm-6">
                      <u><h4 class="font-weight-normal ng-binding">eth_compileSerpent</h4></u>
                    </div>
                    <div class="col-sm-3">
                      <h5 class="font-weight-normal ng-binding ng-hide" ng-show="item.count > 0">Invoked: 0</h5>
                    </div>
                    <div class="col-sm-3 m-l-none">
                      <h5 class="font-weight-normal ng-binding ng-hide" ng-show="item.lastTime">Last call: </h5>
                    </div>
                  </div>
                </div>

                <div class="panel-footer p-b-none p-t-none">
                  <!-- Last Result -->
                  <div class="rpc-item-header ng-hide" ng-show="item.lastResult != null">
                    <a href="#" ng-click="showLastResult(item)">
                      <div class="header-icon m-r-md" style="margin-right: 8px;">
                        <i class="pe page-header-icon pe-7s-plus"></i>
                      </div>
                      <div class="header-title m-l-md"><h5 class="rpc-item-text">Last Result</h5>
                      </div>
                    </a>
                  </div>

                  <div class="rpc-item-result-eth_compileSerpent ng-hide"
                       ng-show="item.lastResult != null &amp;&amp; item.isLastResultVisible">
                    <pre class="panel panel-black-filled rpc-item-result ng-binding">null</pre>
                  </div>

                  <!-- Usage Sample -->
                  <div class="rpc-item-header flex-row flex-align-center rpc-usage">
                    <!--<a href="#" ng-click="showUsageHelp(item.methodName)">-->
                    <div class="header-icon m-l-none m-r-xs">
                      <i class="pe page-header-icon pe-7s-study"></i>
                    </div>
                    <pre class="panel panel-black-filled m-t-xs m-b-xs ng-binding">curl -X POST --data '{"jsonrpc":"2.0","method":"eth_compileSerpent","params":["/* some serpent */"],"id":1}' <span
                      class="ng-binding">http://localhost:8080/rpc</span></pre>
                    <!--<div class="header-title"><h5 class="rpc-item-text">Curl</h5>-->
                    <!--</div>-->
                    <!--</a>-->

                  </div>
                </div>
              </div>
            </il><!-- end ngRepeat: item in rpcItems | rpcItemFilter:filterWord -->
            <il ng-repeat="item in rpcItems | rpcItemFilter:filterWord" class="ng-scope">
              <div class="panel panel-dark-filled">
                <div class="panel-heading p-b-none p-t-none">
                  <div class="row">
                    <div class="col-sm-6">
                      <u><h4 class="font-weight-normal ng-binding">eth_compileSolidity</h4></u>
                    </div>
                    <div class="col-sm-3">
                      <h5 class="font-weight-normal ng-binding ng-hide" ng-show="item.count > 0">Invoked: 0</h5>
                    </div>
                    <div class="col-sm-3 m-l-none">
                      <h5 class="font-weight-normal ng-binding ng-hide" ng-show="item.lastTime">Last call: </h5>
                    </div>
                  </div>
                </div>

                <div class="panel-footer p-b-none p-t-none">
                  <!-- Last Result -->
                  <div class="rpc-item-header ng-hide" ng-show="item.lastResult != null">
                    <a href="#" ng-click="showLastResult(item)">
                      <div class="header-icon m-r-md" style="margin-right: 8px;">
                        <i class="pe page-header-icon pe-7s-plus"></i>
                      </div>
                      <div class="header-title m-l-md"><h5 class="rpc-item-text">Last Result</h5>
                      </div>
                    </a>
                  </div>

                  <div class="rpc-item-result-eth_compileSolidity ng-hide"
                       ng-show="item.lastResult != null &amp;&amp; item.isLastResultVisible">
                    <pre class="panel panel-black-filled rpc-item-result ng-binding">null</pre>
                  </div>

                  <!-- Usage Sample -->
                  <div class="rpc-item-header flex-row flex-align-center rpc-usage">
                    <!--<a href="#" ng-click="showUsageHelp(item.methodName)">-->
                    <div class="header-icon m-l-none m-r-xs">
                      <i class="pe page-header-icon pe-7s-study"></i>
                    </div>
                    <pre class="panel panel-black-filled m-t-xs m-b-xs ng-binding">curl -X POST --data '{"jsonrpc":"2.0","method":"eth_compileSolidity","params":["contract test { function multiply(uint a) returns(uint d) {   return a * 7;   } }"],"id":1}' <span
                      class="ng-binding">http://localhost:8080/rpc</span></pre>
                    <!--<div class="header-title"><h5 class="rpc-item-text">Curl</h5>-->
                    <!--</div>-->
                    <!--</a>-->

                  </div>
                </div>
              </div>
            </il><!-- end ngRepeat: item in rpcItems | rpcItemFilter:filterWord -->
            <il ng-repeat="item in rpcItems | rpcItemFilter:filterWord" class="ng-scope">
              <div class="panel panel-dark-filled">
                <div class="panel-heading p-b-none p-t-none">
                  <div class="row">
                    <div class="col-sm-6">
                      <u><h4 class="font-weight-normal ng-binding">eth_estimateGas</h4></u>
                    </div>
                    <div class="col-sm-3">
                      <h5 class="font-weight-normal ng-binding ng-hide" ng-show="item.count > 0">Invoked: 0</h5>
                    </div>
                    <div class="col-sm-3 m-l-none">
                      <h5 class="font-weight-normal ng-binding ng-hide" ng-show="item.lastTime">Last call: </h5>
                    </div>
                  </div>
                </div>

                <div class="panel-footer p-b-none p-t-none">
                  <!-- Last Result -->
                  <div class="rpc-item-header ng-hide" ng-show="item.lastResult != null">
                    <a href="#" ng-click="showLastResult(item)">
                      <div class="header-icon m-r-md" style="margin-right: 8px;">
                        <i class="pe page-header-icon pe-7s-plus"></i>
                      </div>
                      <div class="header-title m-l-md"><h5 class="rpc-item-text">Last Result</h5>
                      </div>
                    </a>
                  </div>

                  <div class="rpc-item-result-eth_estimateGas ng-hide"
                       ng-show="item.lastResult != null &amp;&amp; item.isLastResultVisible">
                    <pre class="panel panel-black-filled rpc-item-result ng-binding">null</pre>
                  </div>

                  <!-- Usage Sample -->
                  <div class="rpc-item-header flex-row flex-align-center rpc-usage">
                    <!--<a href="#" ng-click="showUsageHelp(item.methodName)">-->
                    <div class="header-icon m-l-none m-r-xs">
                      <i class="pe page-header-icon pe-7s-study"></i>
                    </div>
                    <pre class="panel panel-black-filled m-t-xs m-b-xs ng-binding">curl -X POST --data '{"jsonrpc":"2.0","method":"eth_estimateGas","params":[{"from":"0xcd2a3d9f938e13cd947ec05abc7fe734df8dd826", "to":"0x79b08ad8787060333663d19704909ee7b1903e58", "gas":"0x300000", "gasPrice":"0x10000000000", "value":"0x7777", "data":"0x", "nounce":"0x101F15"}],"id":1}' <span
                      class="ng-binding">http://localhost:8080/rpc</span></pre>
                    <!--<div class="header-title"><h5 class="rpc-item-text">Curl</h5>-->
                    <!--</div>-->
                    <!--</a>-->

                  </div>
                </div>
              </div>
            </il><!-- end ngRepeat: item in rpcItems | rpcItemFilter:filterWord -->
            <il ng-repeat="item in rpcItems | rpcItemFilter:filterWord" class="ng-scope">
              <div class="panel panel-dark-filled">
                <div class="panel-heading p-b-none p-t-none">
                  <div class="row">
                    <div class="col-sm-6">
                      <u><h4 class="font-weight-normal ng-binding">eth_gasPrice</h4></u>
                    </div>
                    <div class="col-sm-3">
                      <h5 class="font-weight-normal ng-binding ng-hide" ng-show="item.count > 0">Invoked: 0</h5>
                    </div>
                    <div class="col-sm-3 m-l-none">
                      <h5 class="font-weight-normal ng-binding ng-hide" ng-show="item.lastTime">Last call: </h5>
                    </div>
                  </div>
                </div>

                <div class="panel-footer p-b-none p-t-none">
                  <!-- Last Result -->
                  <div class="rpc-item-header ng-hide" ng-show="item.lastResult != null">
                    <a href="#" ng-click="showLastResult(item)">
                      <div class="header-icon m-r-md" style="margin-right: 8px;">
                        <i class="pe page-header-icon pe-7s-plus"></i>
                      </div>
                      <div class="header-title m-l-md"><h5 class="rpc-item-text">Last Result</h5>
                      </div>
                    </a>
                  </div>

                  <div class="rpc-item-result-eth_gasPrice ng-hide"
                       ng-show="item.lastResult != null &amp;&amp; item.isLastResultVisible">
                    <pre class="panel panel-black-filled rpc-item-result ng-binding">null</pre>
                  </div>

                  <!-- Usage Sample -->
                  <div class="rpc-item-header flex-row flex-align-center rpc-usage">
                    <!--<a href="#" ng-click="showUsageHelp(item.methodName)">-->
                    <div class="header-icon m-l-none m-r-xs">
                      <i class="pe page-header-icon pe-7s-study"></i>
                    </div>
                    <pre class="panel panel-black-filled m-t-xs m-b-xs ng-binding">curl -X POST --data '{"jsonrpc":"2.0","method":"eth_gasPrice","params":[],"id":73}' <span
                      class="ng-binding">http://localhost:8080/rpc</span></pre>
                    <!--<div class="header-title"><h5 class="rpc-item-text">Curl</h5>-->
                    <!--</div>-->
                    <!--</a>-->

                  </div>
                </div>
              </div>
            </il><!-- end ngRepeat: item in rpcItems | rpcItemFilter:filterWord -->
            <il ng-repeat="item in rpcItems | rpcItemFilter:filterWord" class="ng-scope">
              <div class="panel panel-dark-filled">
                <div class="panel-heading p-b-none p-t-none">
                  <div class="row">
                    <div class="col-sm-6">
                      <u><h4 class="font-weight-normal ng-binding">eth_getBalance</h4></u>
                    </div>
                    <div class="col-sm-3">
                      <h5 class="font-weight-normal ng-binding ng-hide" ng-show="item.count > 0">Invoked: 0</h5>
                    </div>
                    <div class="col-sm-3 m-l-none">
                      <h5 class="font-weight-normal ng-binding ng-hide" ng-show="item.lastTime">Last call: </h5>
                    </div>
                  </div>
                </div>

                <div class="panel-footer p-b-none p-t-none">
                  <!-- Last Result -->
                  <div class="rpc-item-header ng-hide" ng-show="item.lastResult != null">
                    <a href="#" ng-click="showLastResult(item)">
                      <div class="header-icon m-r-md" style="margin-right: 8px;">
                        <i class="pe page-header-icon pe-7s-plus"></i>
                      </div>
                      <div class="header-title m-l-md"><h5 class="rpc-item-text">Last Result</h5>
                      </div>
                    </a>
                  </div>

                  <div class="rpc-item-result-eth_getBalance ng-hide"
                       ng-show="item.lastResult != null &amp;&amp; item.isLastResultVisible">
                    <pre class="panel panel-black-filled rpc-item-result ng-binding">null</pre>
                  </div>

                  <!-- Usage Sample -->
                  <div class="rpc-item-header flex-row flex-align-center rpc-usage">
                    <!--<a href="#" ng-click="showUsageHelp(item.methodName)">-->
                    <div class="header-icon m-l-none m-r-xs">
                      <i class="pe page-header-icon pe-7s-study"></i>
                    </div>
                    <pre class="panel panel-black-filled m-t-xs m-b-xs ng-binding">curl -X POST --data '{"jsonrpc":"2.0","method":"eth_getBalance","params":["0x407d73d8a49eeb85d32cf465507dd71d507100c1", "latest"],"id":1}' <span
                      class="ng-binding">http://localhost:8080/rpc</span></pre>
                    <!--<div class="header-title"><h5 class="rpc-item-text">Curl</h5>-->
                    <!--</div>-->
                    <!--</a>-->

                  </div>
                </div>
              </div>
            </il><!-- end ngRepeat: item in rpcItems | rpcItemFilter:filterWord -->
            <il ng-repeat="item in rpcItems | rpcItemFilter:filterWord" class="ng-scope">
              <div class="panel panel-dark-filled">
                <div class="panel-heading p-b-none p-t-none">
                  <div class="row">
                    <div class="col-sm-6">
                      <u><h4 class="font-weight-normal ng-binding">eth_getBlockByHash</h4></u>
                    </div>
                    <div class="col-sm-3">
                      <h5 class="font-weight-normal ng-binding ng-hide" ng-show="item.count > 0">Invoked: 0</h5>
                    </div>
                    <div class="col-sm-3 m-l-none">
                      <h5 class="font-weight-normal ng-binding ng-hide" ng-show="item.lastTime">Last call: </h5>
                    </div>
                  </div>
                </div>

                <div class="panel-footer p-b-none p-t-none">
                  <!-- Last Result -->
                  <div class="rpc-item-header ng-hide" ng-show="item.lastResult != null">
                    <a href="#" ng-click="showLastResult(item)">
                      <div class="header-icon m-r-md" style="margin-right: 8px;">
                        <i class="pe page-header-icon pe-7s-plus"></i>
                      </div>
                      <div class="header-title m-l-md"><h5 class="rpc-item-text">Last Result</h5>
                      </div>
                    </a>
                  </div>

                  <div class="rpc-item-result-eth_getBlockByHash ng-hide"
                       ng-show="item.lastResult != null &amp;&amp; item.isLastResultVisible">
                    <pre class="panel panel-black-filled rpc-item-result ng-binding">null</pre>
                  </div>

                  <!-- Usage Sample -->
                  <div class="rpc-item-header flex-row flex-align-center rpc-usage">
                    <!--<a href="#" ng-click="showUsageHelp(item.methodName)">-->
                    <div class="header-icon m-l-none m-r-xs">
                      <i class="pe page-header-icon pe-7s-study"></i>
                    </div>
                    <pre class="panel panel-black-filled m-t-xs m-b-xs ng-binding">curl -X POST --data '{"jsonrpc":"2.0","method":"eth_getBlockByHash","params":["0xe670ec64341771606e55d6b4ca35a1a6b75ee3d5145a99d05921026d1527331", true],"id":1}' <span
                      class="ng-binding">http://localhost:8080/rpc</span></pre>
                    <!--<div class="header-title"><h5 class="rpc-item-text">Curl</h5>-->
                    <!--</div>-->
                    <!--</a>-->

                  </div>
                </div>
              </div>
            </il><!-- end ngRepeat: item in rpcItems | rpcItemFilter:filterWord -->
            <il ng-repeat="item in rpcItems | rpcItemFilter:filterWord" class="ng-scope">
              <div class="panel panel-dark-filled">
                <div class="panel-heading p-b-none p-t-none">
                  <div class="row">
                    <div class="col-sm-6">
                      <u><h4 class="font-weight-normal ng-binding">eth_getBlockByNumber</h4></u>
                    </div>
                    <div class="col-sm-3">
                      <h5 class="font-weight-normal ng-binding ng-hide" ng-show="item.count > 0">Invoked: 0</h5>
                    </div>
                    <div class="col-sm-3 m-l-none">
                      <h5 class="font-weight-normal ng-binding ng-hide" ng-show="item.lastTime">Last call: </h5>
                    </div>
                  </div>
                </div>

                <div class="panel-footer p-b-none p-t-none">
                  <!-- Last Result -->
                  <div class="rpc-item-header ng-hide" ng-show="item.lastResult != null">
                    <a href="#" ng-click="showLastResult(item)">
                      <div class="header-icon m-r-md" style="margin-right: 8px;">
                        <i class="pe page-header-icon pe-7s-plus"></i>
                      </div>
                      <div class="header-title m-l-md"><h5 class="rpc-item-text">Last Result</h5>
                      </div>
                    </a>
                  </div>

                  <div class="rpc-item-result-eth_getBlockByNumber ng-hide"
                       ng-show="item.lastResult != null &amp;&amp; item.isLastResultVisible">
                    <pre class="panel panel-black-filled rpc-item-result ng-binding">null</pre>
                  </div>

                  <!-- Usage Sample -->
                  <div class="rpc-item-header flex-row flex-align-center rpc-usage">
                    <!--<a href="#" ng-click="showUsageHelp(item.methodName)">-->
                    <div class="header-icon m-l-none m-r-xs">
                      <i class="pe page-header-icon pe-7s-study"></i>
                    </div>
                    <pre class="panel panel-black-filled m-t-xs m-b-xs ng-binding">curl -X POST --data '{"jsonrpc":"2.0","method":"eth_getBlockByNumber","params":["0x1b4", true],"id":1}' <span
                      class="ng-binding">http://localhost:8080/rpc</span></pre>
                    <!--<div class="header-title"><h5 class="rpc-item-text">Curl</h5>-->
                    <!--</div>-->
                    <!--</a>-->

                  </div>
                </div>
              </div>
            </il><!-- end ngRepeat: item in rpcItems | rpcItemFilter:filterWord -->
            <il ng-repeat="item in rpcItems | rpcItemFilter:filterWord" class="ng-scope">
              <div class="panel panel-dark-filled">
                <div class="panel-heading p-b-none p-t-none">
                  <div class="row">
                    <div class="col-sm-6">
                      <u><h4 class="font-weight-normal ng-binding">eth_getBlockTransactionCountByHash</h4></u>
                    </div>
                    <div class="col-sm-3">
                      <h5 class="font-weight-normal ng-binding ng-hide" ng-show="item.count > 0">Invoked: 0</h5>
                    </div>
                    <div class="col-sm-3 m-l-none">
                      <h5 class="font-weight-normal ng-binding ng-hide" ng-show="item.lastTime">Last call: </h5>
                    </div>
                  </div>
                </div>

                <div class="panel-footer p-b-none p-t-none">
                  <!-- Last Result -->
                  <div class="rpc-item-header ng-hide" ng-show="item.lastResult != null">
                    <a href="#" ng-click="showLastResult(item)">
                      <div class="header-icon m-r-md" style="margin-right: 8px;">
                        <i class="pe page-header-icon pe-7s-plus"></i>
                      </div>
                      <div class="header-title m-l-md"><h5 class="rpc-item-text">Last Result</h5>
                      </div>
                    </a>
                  </div>

                  <div class="rpc-item-result-eth_getBlockTransactionCountByHash ng-hide"
                       ng-show="item.lastResult != null &amp;&amp; item.isLastResultVisible">
                    <pre class="panel panel-black-filled rpc-item-result ng-binding">null</pre>
                  </div>

                  <!-- Usage Sample -->
                  <div class="rpc-item-header flex-row flex-align-center rpc-usage">
                    <!--<a href="#" ng-click="showUsageHelp(item.methodName)">-->
                    <div class="header-icon m-l-none m-r-xs">
                      <i class="pe page-header-icon pe-7s-study"></i>
                    </div>
                    <pre class="panel panel-black-filled m-t-xs m-b-xs ng-binding">curl -X POST --data '{"jsonrpc":"2.0","method":"eth_getBlockTransactionCountByHash","params":["0xb903239f8543d04b5dc1ba6579132b143087c68db1b2168786408fcbce568238"],"id":1}' <span
                      class="ng-binding">http://localhost:8080/rpc</span></pre>
                    <!--<div class="header-title"><h5 class="rpc-item-text">Curl</h5>-->
                    <!--</div>-->
                    <!--</a>-->

                  </div>
                </div>
              </div>
            </il><!-- end ngRepeat: item in rpcItems | rpcItemFilter:filterWord -->
            <il ng-repeat="item in rpcItems | rpcItemFilter:filterWord" class="ng-scope">
              <div class="panel panel-dark-filled">
                <div class="panel-heading p-b-none p-t-none">
                  <div class="row">
                    <div class="col-sm-6">
                      <u><h4 class="font-weight-normal ng-binding">eth_getBlockTransactionCountByNumber</h4></u>
                    </div>
                    <div class="col-sm-3">
                      <h5 class="font-weight-normal ng-binding ng-hide" ng-show="item.count > 0">Invoked: 0</h5>
                    </div>
                    <div class="col-sm-3 m-l-none">
                      <h5 class="font-weight-normal ng-binding ng-hide" ng-show="item.lastTime">Last call: </h5>
                    </div>
                  </div>
                </div>

                <div class="panel-footer p-b-none p-t-none">
                  <!-- Last Result -->
                  <div class="rpc-item-header ng-hide" ng-show="item.lastResult != null">
                    <a href="#" ng-click="showLastResult(item)">
                      <div class="header-icon m-r-md" style="margin-right: 8px;">
                        <i class="pe page-header-icon pe-7s-plus"></i>
                      </div>
                      <div class="header-title m-l-md"><h5 class="rpc-item-text">Last Result</h5>
                      </div>
                    </a>
                  </div>

                  <div class="rpc-item-result-eth_getBlockTransactionCountByNumber ng-hide"
                       ng-show="item.lastResult != null &amp;&amp; item.isLastResultVisible">
                    <pre class="panel panel-black-filled rpc-item-result ng-binding">null</pre>
                  </div>

                  <!-- Usage Sample -->
                  <div class="rpc-item-header flex-row flex-align-center rpc-usage">
                    <!--<a href="#" ng-click="showUsageHelp(item.methodName)">-->
                    <div class="header-icon m-l-none m-r-xs">
                      <i class="pe page-header-icon pe-7s-study"></i>
                    </div>
                    <pre class="panel panel-black-filled m-t-xs m-b-xs ng-binding">curl -X POST --data '{"jsonrpc":"2.0","method":"eth_getBlockTransactionCountByNumber","params":["0xe8"],"id":1}' <span
                      class="ng-binding">http://localhost:8080/rpc</span></pre>
                    <!--<div class="header-title"><h5 class="rpc-item-text">Curl</h5>-->
                    <!--</div>-->
                    <!--</a>-->

                  </div>
                </div>
              </div>
            </il><!-- end ngRepeat: item in rpcItems | rpcItemFilter:filterWord -->
            <il ng-repeat="item in rpcItems | rpcItemFilter:filterWord" class="ng-scope">
              <div class="panel panel-dark-filled">
                <div class="panel-heading p-b-none p-t-none">
                  <div class="row">
                    <div class="col-sm-6">
                      <u><h4 class="font-weight-normal ng-binding">eth_getCode</h4></u>
                    </div>
                    <div class="col-sm-3">
                      <h5 class="font-weight-normal ng-binding ng-hide" ng-show="item.count > 0">Invoked: 0</h5>
                    </div>
                    <div class="col-sm-3 m-l-none">
                      <h5 class="font-weight-normal ng-binding ng-hide" ng-show="item.lastTime">Last call: </h5>
                    </div>
                  </div>
                </div>

                <div class="panel-footer p-b-none p-t-none">
                  <!-- Last Result -->
                  <div class="rpc-item-header ng-hide" ng-show="item.lastResult != null">
                    <a href="#" ng-click="showLastResult(item)">
                      <div class="header-icon m-r-md" style="margin-right: 8px;">
                        <i class="pe page-header-icon pe-7s-plus"></i>
                      </div>
                      <div class="header-title m-l-md"><h5 class="rpc-item-text">Last Result</h5>
                      </div>
                    </a>
                  </div>

                  <div class="rpc-item-result-eth_getCode ng-hide"
                       ng-show="item.lastResult != null &amp;&amp; item.isLastResultVisible">
                    <pre class="panel panel-black-filled rpc-item-result ng-binding">null</pre>
                  </div>

                  <!-- Usage Sample -->
                  <div class="rpc-item-header flex-row flex-align-center rpc-usage">
                    <!--<a href="#" ng-click="showUsageHelp(item.methodName)">-->
                    <div class="header-icon m-l-none m-r-xs">
                      <i class="pe page-header-icon pe-7s-study"></i>
                    </div>
                    <pre class="panel panel-black-filled m-t-xs m-b-xs ng-binding">curl -X POST --data '{"jsonrpc":"2.0","method":"eth_getCode","params":["0xa94f5374fce5edbc8e2a8697c15331677e6ebf0b", "0x2"],"id":1}' <span
                      class="ng-binding">http://localhost:8080/rpc</span></pre>
                    <!--<div class="header-title"><h5 class="rpc-item-text">Curl</h5>-->
                    <!--</div>-->
                    <!--</a>-->

                  </div>
                </div>
              </div>
            </il><!-- end ngRepeat: item in rpcItems | rpcItemFilter:filterWord -->
            <il ng-repeat="item in rpcItems | rpcItemFilter:filterWord" class="ng-scope">
              <div class="panel panel-dark-filled">
                <div class="panel-heading p-b-none p-t-none">
                  <div class="row">
                    <div class="col-sm-6">
                      <u><h4 class="font-weight-normal ng-binding">eth_getCompilers</h4></u>
                    </div>
                    <div class="col-sm-3">
                      <h5 class="font-weight-normal ng-binding ng-hide" ng-show="item.count > 0">Invoked: 0</h5>
                    </div>
                    <div class="col-sm-3 m-l-none">
                      <h5 class="font-weight-normal ng-binding ng-hide" ng-show="item.lastTime">Last call: </h5>
                    </div>
                  </div>
                </div>

                <div class="panel-footer p-b-none p-t-none">
                  <!-- Last Result -->
                  <div class="rpc-item-header ng-hide" ng-show="item.lastResult != null">
                    <a href="#" ng-click="showLastResult(item)">
                      <div class="header-icon m-r-md" style="margin-right: 8px;">
                        <i class="pe page-header-icon pe-7s-plus"></i>
                      </div>
                      <div class="header-title m-l-md"><h5 class="rpc-item-text">Last Result</h5>
                      </div>
                    </a>
                  </div>

                  <div class="rpc-item-result-eth_getCompilers ng-hide"
                       ng-show="item.lastResult != null &amp;&amp; item.isLastResultVisible">
                    <pre class="panel panel-black-filled rpc-item-result ng-binding">null</pre>
                  </div>

                  <!-- Usage Sample -->
                  <div class="rpc-item-header flex-row flex-align-center rpc-usage">
                    <!--<a href="#" ng-click="showUsageHelp(item.methodName)">-->
                    <div class="header-icon m-l-none m-r-xs">
                      <i class="pe page-header-icon pe-7s-study"></i>
                    </div>
                    <pre class="panel panel-black-filled m-t-xs m-b-xs ng-binding">curl -X POST --data '{"jsonrpc":"2.0","method":"eth_getCompilers","params":[],"id":1}' <span
                      class="ng-binding">http://localhost:8080/rpc</span></pre>
                    <!--<div class="header-title"><h5 class="rpc-item-text">Curl</h5>-->
                    <!--</div>-->
                    <!--</a>-->

                  </div>
                </div>
              </div>
            </il><!-- end ngRepeat: item in rpcItems | rpcItemFilter:filterWord -->
            <il ng-repeat="item in rpcItems | rpcItemFilter:filterWord" class="ng-scope">
              <div class="panel panel-dark-filled">
                <div class="panel-heading p-b-none p-t-none">
                  <div class="row">
                    <div class="col-sm-6">
                      <u><h4 class="font-weight-normal ng-binding">eth_getFilterChanges</h4></u>
                    </div>
                    <div class="col-sm-3">
                      <h5 class="font-weight-normal ng-binding ng-hide" ng-show="item.count > 0">Invoked: 0</h5>
                    </div>
                    <div class="col-sm-3 m-l-none">
                      <h5 class="font-weight-normal ng-binding ng-hide" ng-show="item.lastTime">Last call: </h5>
                    </div>
                  </div>
                </div>

                <div class="panel-footer p-b-none p-t-none">
                  <!-- Last Result -->
                  <div class="rpc-item-header ng-hide" ng-show="item.lastResult != null">
                    <a href="#" ng-click="showLastResult(item)">
                      <div class="header-icon m-r-md" style="margin-right: 8px;">
                        <i class="pe page-header-icon pe-7s-plus"></i>
                      </div>
                      <div class="header-title m-l-md"><h5 class="rpc-item-text">Last Result</h5>
                      </div>
                    </a>
                  </div>

                  <div class="rpc-item-result-eth_getFilterChanges ng-hide"
                       ng-show="item.lastResult != null &amp;&amp; item.isLastResultVisible">
                    <pre class="panel panel-black-filled rpc-item-result ng-binding">null</pre>
                  </div>

                  <!-- Usage Sample -->
                  <div class="rpc-item-header flex-row flex-align-center rpc-usage">
                    <!--<a href="#" ng-click="showUsageHelp(item.methodName)">-->
                    <div class="header-icon m-l-none m-r-xs">
                      <i class="pe page-header-icon pe-7s-study"></i>
                    </div>
                    <pre class="panel panel-black-filled m-t-xs m-b-xs ng-binding">curl -X POST --data '{"jsonrpc":"2.0","method":"eth_getFilterChanges","params":["0x16"],"id":73}' <span
                      class="ng-binding">http://localhost:8080/rpc</span></pre>
                    <!--<div class="header-title"><h5 class="rpc-item-text">Curl</h5>-->
                    <!--</div>-->
                    <!--</a>-->

                  </div>
                </div>
              </div>
            </il><!-- end ngRepeat: item in rpcItems | rpcItemFilter:filterWord -->
            <il ng-repeat="item in rpcItems | rpcItemFilter:filterWord" class="ng-scope">
              <div class="panel panel-dark-filled">
                <div class="panel-heading p-b-none p-t-none">
                  <div class="row">
                    <div class="col-sm-6">
                      <u><h4 class="font-weight-normal ng-binding">eth_getFilterLogs</h4></u>
                    </div>
                    <div class="col-sm-3">
                      <h5 class="font-weight-normal ng-binding ng-hide" ng-show="item.count > 0">Invoked: 0</h5>
                    </div>
                    <div class="col-sm-3 m-l-none">
                      <h5 class="font-weight-normal ng-binding ng-hide" ng-show="item.lastTime">Last call: </h5>
                    </div>
                  </div>
                </div>

                <div class="panel-footer p-b-none p-t-none">
                  <!-- Last Result -->
                  <div class="rpc-item-header ng-hide" ng-show="item.lastResult != null">
                    <a href="#" ng-click="showLastResult(item)">
                      <div class="header-icon m-r-md" style="margin-right: 8px;">
                        <i class="pe page-header-icon pe-7s-plus"></i>
                      </div>
                      <div class="header-title m-l-md"><h5 class="rpc-item-text">Last Result</h5>
                      </div>
                    </a>
                  </div>

                  <div class="rpc-item-result-eth_getFilterLogs ng-hide"
                       ng-show="item.lastResult != null &amp;&amp; item.isLastResultVisible">
                    <pre class="panel panel-black-filled rpc-item-result ng-binding">null</pre>
                  </div>

                  <!-- Usage Sample -->
                  <div class="rpc-item-header flex-row flex-align-center rpc-usage">
                    <!--<a href="#" ng-click="showUsageHelp(item.methodName)">-->
                    <div class="header-icon m-l-none m-r-xs">
                      <i class="pe page-header-icon pe-7s-study"></i>
                    </div>
                    <pre class="panel panel-black-filled m-t-xs m-b-xs ng-binding">curl -X POST --data '{"jsonrpc":"2.0","method":"eth_getFilterLogs","params":["0x16"],"id":74}' <span
                      class="ng-binding">http://localhost:8080/rpc</span></pre>
                    <!--<div class="header-title"><h5 class="rpc-item-text">Curl</h5>-->
                    <!--</div>-->
                    <!--</a>-->

                  </div>
                </div>
              </div>
            </il><!-- end ngRepeat: item in rpcItems | rpcItemFilter:filterWord -->
            <il ng-repeat="item in rpcItems | rpcItemFilter:filterWord" class="ng-scope">
              <div class="panel panel-dark-filled">
                <div class="panel-heading p-b-none p-t-none">
                  <div class="row">
                    <div class="col-sm-6">
                      <u><h4 class="font-weight-normal ng-binding">eth_getLastBalance</h4></u>
                    </div>
                    <div class="col-sm-3">
                      <h5 class="font-weight-normal ng-binding ng-hide" ng-show="item.count > 0">Invoked: 0</h5>
                    </div>
                    <div class="col-sm-3 m-l-none">
                      <h5 class="font-weight-normal ng-binding ng-hide" ng-show="item.lastTime">Last call: </h5>
                    </div>
                  </div>
                </div>

                <div class="panel-footer p-b-none p-t-none">
                  <!-- Last Result -->
                  <div class="rpc-item-header ng-hide" ng-show="item.lastResult != null">
                    <a href="#" ng-click="showLastResult(item)">
                      <div class="header-icon m-r-md" style="margin-right: 8px;">
                        <i class="pe page-header-icon pe-7s-plus"></i>
                      </div>
                      <div class="header-title m-l-md"><h5 class="rpc-item-text">Last Result</h5>
                      </div>
                    </a>
                  </div>

                  <div class="rpc-item-result-eth_getLastBalance ng-hide"
                       ng-show="item.lastResult != null &amp;&amp; item.isLastResultVisible">
                    <pre class="panel panel-black-filled rpc-item-result ng-binding">null</pre>
                  </div>

                  <!-- Usage Sample -->
                  <div class="rpc-item-header flex-row flex-align-center rpc-usage">
                    <!--<a href="#" ng-click="showUsageHelp(item.methodName)">-->
                    <div class="header-icon m-l-none m-r-xs">
                      <i class="pe page-header-icon pe-7s-study"></i>
                    </div>
                    <pre class="panel panel-black-filled m-t-xs m-b-xs ng-binding">curl -X POST --data '{"jsonrpc":"2.0","method":"eth_getLastBalance","params":["0x0"],"id":64}' <span
                      class="ng-binding">http://localhost:8080/rpc</span></pre>
                    <!--<div class="header-title"><h5 class="rpc-item-text">Curl</h5>-->
                    <!--</div>-->
                    <!--</a>-->

                  </div>
                </div>
              </div>
            </il><!-- end ngRepeat: item in rpcItems | rpcItemFilter:filterWord -->
            <il ng-repeat="item in rpcItems | rpcItemFilter:filterWord" class="ng-scope">
              <div class="panel panel-dark-filled">
                <div class="panel-heading p-b-none p-t-none">
                  <div class="row">
                    <div class="col-sm-6">
                      <u><h4 class="font-weight-normal ng-binding">eth_getLogs</h4></u>
                    </div>
                    <div class="col-sm-3">
                      <h5 class="font-weight-normal ng-binding ng-hide" ng-show="item.count > 0">Invoked: 0</h5>
                    </div>
                    <div class="col-sm-3 m-l-none">
                      <h5 class="font-weight-normal ng-binding ng-hide" ng-show="item.lastTime">Last call: </h5>
                    </div>
                  </div>
                </div>

                <div class="panel-footer p-b-none p-t-none">
                  <!-- Last Result -->
                  <div class="rpc-item-header ng-hide" ng-show="item.lastResult != null">
                    <a href="#" ng-click="showLastResult(item)">
                      <div class="header-icon m-r-md" style="margin-right: 8px;">
                        <i class="pe page-header-icon pe-7s-plus"></i>
                      </div>
                      <div class="header-title m-l-md"><h5 class="rpc-item-text">Last Result</h5>
                      </div>
                    </a>
                  </div>

                  <div class="rpc-item-result-eth_getLogs ng-hide"
                       ng-show="item.lastResult != null &amp;&amp; item.isLastResultVisible">
                    <pre class="panel panel-black-filled rpc-item-result ng-binding">null</pre>
                  </div>

                  <!-- Usage Sample -->
                  <div class="rpc-item-header flex-row flex-align-center rpc-usage">
                    <!--<a href="#" ng-click="showUsageHelp(item.methodName)">-->
                    <div class="header-icon m-l-none m-r-xs">
                      <i class="pe page-header-icon pe-7s-study"></i>
                    </div>
                    <pre class="panel panel-black-filled m-t-xs m-b-xs ng-binding">curl -X POST --data '{"jsonrpc":"2.0","method":"eth_getLogs","params":[{"topics":["0x000000000000000000000000a94f5374fce5edbc8e2a8697c15331677e6ebf0b"]}],"id":74}' <span
                      class="ng-binding">http://localhost:8080/rpc</span></pre>
                    <!--<div class="header-title"><h5 class="rpc-item-text">Curl</h5>-->
                    <!--</div>-->
                    <!--</a>-->

                  </div>
                </div>
              </div>
            </il><!-- end ngRepeat: item in rpcItems | rpcItemFilter:filterWord -->
            <il ng-repeat="item in rpcItems | rpcItemFilter:filterWord" class="ng-scope">
              <div class="panel panel-dark-filled">
                <div class="panel-heading p-b-none p-t-none">
                  <div class="row">
                    <div class="col-sm-6">
                      <u><h4 class="font-weight-normal ng-binding">eth_getStorageAt</h4></u>
                    </div>
                    <div class="col-sm-3">
                      <h5 class="font-weight-normal ng-binding ng-hide" ng-show="item.count > 0">Invoked: 0</h5>
                    </div>
                    <div class="col-sm-3 m-l-none">
                      <h5 class="font-weight-normal ng-binding ng-hide" ng-show="item.lastTime">Last call: </h5>
                    </div>
                  </div>
                </div>

                <div class="panel-footer p-b-none p-t-none">
                  <!-- Last Result -->
                  <div class="rpc-item-header ng-hide" ng-show="item.lastResult != null">
                    <a href="#" ng-click="showLastResult(item)">
                      <div class="header-icon m-r-md" style="margin-right: 8px;">
                        <i class="pe page-header-icon pe-7s-plus"></i>
                      </div>
                      <div class="header-title m-l-md"><h5 class="rpc-item-text">Last Result</h5>
                      </div>
                    </a>
                  </div>

                  <div class="rpc-item-result-eth_getStorageAt ng-hide"
                       ng-show="item.lastResult != null &amp;&amp; item.isLastResultVisible">
                    <pre class="panel panel-black-filled rpc-item-result ng-binding">null</pre>
                  </div>

                  <!-- Usage Sample -->
                  <div class="rpc-item-header flex-row flex-align-center rpc-usage">
                    <!--<a href="#" ng-click="showUsageHelp(item.methodName)">-->
                    <div class="header-icon m-l-none m-r-xs">
                      <i class="pe page-header-icon pe-7s-study"></i>
                    </div>
                    <pre class="panel panel-black-filled m-t-xs m-b-xs ng-binding">curl --data '{"id": 1, "method": "eth_getStorageAt", "params": ["0x295a70b2de5e3953354a6a8344e616ed314d7251", "0x0", "latest"]}' localhost:8545 <span
                      class="ng-binding">http://localhost:8080/rpc</span></pre>
                    <!--<div class="header-title"><h5 class="rpc-item-text">Curl</h5>-->
                    <!--</div>-->
                    <!--</a>-->

                  </div>
                </div>
              </div>
            </il><!-- end ngRepeat: item in rpcItems | rpcItemFilter:filterWord -->
            <il ng-repeat="item in rpcItems | rpcItemFilter:filterWord" class="ng-scope">
              <div class="panel panel-dark-filled">
                <div class="panel-heading p-b-none p-t-none">
                  <div class="row">
                    <div class="col-sm-6">
                      <u><h4 class="font-weight-normal ng-binding">eth_getTransactionByBlockHashAndIndex</h4></u>
                    </div>
                    <div class="col-sm-3">
                      <h5 class="font-weight-normal ng-binding ng-hide" ng-show="item.count > 0">Invoked: 0</h5>
                    </div>
                    <div class="col-sm-3 m-l-none">
                      <h5 class="font-weight-normal ng-binding ng-hide" ng-show="item.lastTime">Last call: </h5>
                    </div>
                  </div>
                </div>

                <div class="panel-footer p-b-none p-t-none">
                  <!-- Last Result -->
                  <div class="rpc-item-header ng-hide" ng-show="item.lastResult != null">
                    <a href="#" ng-click="showLastResult(item)">
                      <div class="header-icon m-r-md" style="margin-right: 8px;">
                        <i class="pe page-header-icon pe-7s-plus"></i>
                      </div>
                      <div class="header-title m-l-md"><h5 class="rpc-item-text">Last Result</h5>
                      </div>
                    </a>
                  </div>

                  <div class="rpc-item-result-eth_getTransactionByBlockHashAndIndex ng-hide"
                       ng-show="item.lastResult != null &amp;&amp; item.isLastResultVisible">
                    <pre class="panel panel-black-filled rpc-item-result ng-binding">null</pre>
                  </div>

                  <!-- Usage Sample -->
                  <div class="rpc-item-header flex-row flex-align-center rpc-usage">
                    <!--<a href="#" ng-click="showUsageHelp(item.methodName)">-->
                    <div class="header-icon m-l-none m-r-xs">
                      <i class="pe page-header-icon pe-7s-study"></i>
                    </div>
                    <pre class="panel panel-black-filled m-t-xs m-b-xs ng-binding">curl -X POST --data '{"jsonrpc":"2.0","method":"eth_getTransactionByBlockHashAndIndex","params":[0xc6ef2fc5426d6ad6fd9e2a26abeab0aa2411b7ab17f30a99d3cb96aed1d1055b, "0x0"],"id":1}' <span
                      class="ng-binding">http://localhost:8080/rpc</span></pre>
                    <!--<div class="header-title"><h5 class="rpc-item-text">Curl</h5>-->
                    <!--</div>-->
                    <!--</a>-->

                  </div>
                </div>
              </div>
            </il><!-- end ngRepeat: item in rpcItems | rpcItemFilter:filterWord -->
            <il ng-repeat="item in rpcItems | rpcItemFilter:filterWord" class="ng-scope">
              <div class="panel panel-dark-filled">
                <div class="panel-heading p-b-none p-t-none">
                  <div class="row">
                    <div class="col-sm-6">
                      <u><h4 class="font-weight-normal ng-binding">eth_getTransactionByBlockNumberAndIndex</h4></u>
                    </div>
                    <div class="col-sm-3">
                      <h5 class="font-weight-normal ng-binding ng-hide" ng-show="item.count > 0">Invoked: 0</h5>
                    </div>
                    <div class="col-sm-3 m-l-none">
                      <h5 class="font-weight-normal ng-binding ng-hide" ng-show="item.lastTime">Last call: </h5>
                    </div>
                  </div>
                </div>

                <div class="panel-footer p-b-none p-t-none">
                  <!-- Last Result -->
                  <div class="rpc-item-header ng-hide" ng-show="item.lastResult != null">
                    <a href="#" ng-click="showLastResult(item)">
                      <div class="header-icon m-r-md" style="margin-right: 8px;">
                        <i class="pe page-header-icon pe-7s-plus"></i>
                      </div>
                      <div class="header-title m-l-md"><h5 class="rpc-item-text">Last Result</h5>
                      </div>
                    </a>
                  </div>

                  <div class="rpc-item-result-eth_getTransactionByBlockNumberAndIndex ng-hide"
                       ng-show="item.lastResult != null &amp;&amp; item.isLastResultVisible">
                    <pre class="panel panel-black-filled rpc-item-result ng-binding">null</pre>
                  </div>

                  <!-- Usage Sample -->
                  <div class="rpc-item-header flex-row flex-align-center rpc-usage">
                    <!--<a href="#" ng-click="showUsageHelp(item.methodName)">-->
                    <div class="header-icon m-l-none m-r-xs">
                      <i class="pe page-header-icon pe-7s-study"></i>
                    </div>
                    <pre class="panel panel-black-filled m-t-xs m-b-xs ng-binding">curl -X POST --data '{"jsonrpc":"2.0","method":"eth_getTransactionByBlockNumberAndIndex","params":["0x29c", "0x0"],"id":1}' <span
                      class="ng-binding">http://localhost:8080/rpc</span></pre>
                    <!--<div class="header-title"><h5 class="rpc-item-text">Curl</h5>-->
                    <!--</div>-->
                    <!--</a>-->

                  </div>
                </div>
              </div>
            </il><!-- end ngRepeat: item in rpcItems | rpcItemFilter:filterWord -->
            <il ng-repeat="item in rpcItems | rpcItemFilter:filterWord" class="ng-scope">
              <div class="panel panel-dark-filled">
                <div class="panel-heading p-b-none p-t-none">
                  <div class="row">
                    <div class="col-sm-6">
                      <u><h4 class="font-weight-normal ng-binding">eth_getTransactionByHash</h4></u>
                    </div>
                    <div class="col-sm-3">
                      <h5 class="font-weight-normal ng-binding ng-hide" ng-show="item.count > 0">Invoked: 0</h5>
                    </div>
                    <div class="col-sm-3 m-l-none">
                      <h5 class="font-weight-normal ng-binding ng-hide" ng-show="item.lastTime">Last call: </h5>
                    </div>
                  </div>
                </div>

                <div class="panel-footer p-b-none p-t-none">
                  <!-- Last Result -->
                  <div class="rpc-item-header ng-hide" ng-show="item.lastResult != null">
                    <a href="#" ng-click="showLastResult(item)">
                      <div class="header-icon m-r-md" style="margin-right: 8px;">
                        <i class="pe page-header-icon pe-7s-plus"></i>
                      </div>
                      <div class="header-title m-l-md"><h5 class="rpc-item-text">Last Result</h5>
                      </div>
                    </a>
                  </div>

                  <div class="rpc-item-result-eth_getTransactionByHash ng-hide"
                       ng-show="item.lastResult != null &amp;&amp; item.isLastResultVisible">
                    <pre class="panel panel-black-filled rpc-item-result ng-binding">null</pre>
                  </div>

                  <!-- Usage Sample -->
                  <div class="rpc-item-header flex-row flex-align-center rpc-usage">
                    <!--<a href="#" ng-click="showUsageHelp(item.methodName)">-->
                    <div class="header-icon m-l-none m-r-xs">
                      <i class="pe page-header-icon pe-7s-study"></i>
                    </div>
                    <pre class="panel panel-black-filled m-t-xs m-b-xs ng-binding">curl -X POST --data '{"jsonrpc":"2.0","method":"eth_getTransactionByHash","params":["0xb903239f8543d04b5dc1ba6579132b143087c68db1b2168786408fcbce568238"],"id":1}' <span
                      class="ng-binding">http://localhost:8080/rpc</span></pre>
                    <!--<div class="header-title"><h5 class="rpc-item-text">Curl</h5>-->
                    <!--</div>-->
                    <!--</a>-->

                  </div>
                </div>
              </div>
            </il><!-- end ngRepeat: item in rpcItems | rpcItemFilter:filterWord -->
            <il ng-repeat="item in rpcItems | rpcItemFilter:filterWord" class="ng-scope">
              <div class="panel panel-dark-filled">
                <div class="panel-heading p-b-none p-t-none">
                  <div class="row">
                    <div class="col-sm-6">
                      <u><h4 class="font-weight-normal ng-binding">eth_getTransactionCount</h4></u>
                    </div>
                    <div class="col-sm-3">
                      <h5 class="font-weight-normal ng-binding ng-hide" ng-show="item.count > 0">Invoked: 0</h5>
                    </div>
                    <div class="col-sm-3 m-l-none">
                      <h5 class="font-weight-normal ng-binding ng-hide" ng-show="item.lastTime">Last call: </h5>
                    </div>
                  </div>
                </div>

                <div class="panel-footer p-b-none p-t-none">
                  <!-- Last Result -->
                  <div class="rpc-item-header ng-hide" ng-show="item.lastResult != null">
                    <a href="#" ng-click="showLastResult(item)">
                      <div class="header-icon m-r-md" style="margin-right: 8px;">
                        <i class="pe page-header-icon pe-7s-plus"></i>
                      </div>
                      <div class="header-title m-l-md"><h5 class="rpc-item-text">Last Result</h5>
                      </div>
                    </a>
                  </div>

                  <div class="rpc-item-result-eth_getTransactionCount ng-hide"
                       ng-show="item.lastResult != null &amp;&amp; item.isLastResultVisible">
                    <pre class="panel panel-black-filled rpc-item-result ng-binding">null</pre>
                  </div>

                  <!-- Usage Sample -->
                  <div class="rpc-item-header flex-row flex-align-center rpc-usage">
                    <!--<a href="#" ng-click="showUsageHelp(item.methodName)">-->
                    <div class="header-icon m-l-none m-r-xs">
                      <i class="pe page-header-icon pe-7s-study"></i>
                    </div>
                    <pre class="panel panel-black-filled m-t-xs m-b-xs ng-binding">curl -X POST --data '{"jsonrpc":"2.0","method":"eth_getTransactionCount","params":["0x407d73d8a49eeb85d32cf465507dd71d507100c1","latest"],"id":1}' <span
                      class="ng-binding">http://localhost:8080/rpc</span></pre>
                    <!--<div class="header-title"><h5 class="rpc-item-text">Curl</h5>-->
                    <!--</div>-->
                    <!--</a>-->

                  </div>
                </div>
              </div>
            </il><!-- end ngRepeat: item in rpcItems | rpcItemFilter:filterWord -->
            <il ng-repeat="item in rpcItems | rpcItemFilter:filterWord" class="ng-scope">
              <div class="panel panel-dark-filled">
                <div class="panel-heading p-b-none p-t-none">
                  <div class="row">
                    <div class="col-sm-6">
                      <u><h4 class="font-weight-normal ng-binding">eth_getTransactionReceipt</h4></u>
                    </div>
                    <div class="col-sm-3">
                      <h5 class="font-weight-normal ng-binding ng-hide" ng-show="item.count > 0">Invoked: 0</h5>
                    </div>
                    <div class="col-sm-3 m-l-none">
                      <h5 class="font-weight-normal ng-binding ng-hide" ng-show="item.lastTime">Last call: </h5>
                    </div>
                  </div>
                </div>

                <div class="panel-footer p-b-none p-t-none">
                  <!-- Last Result -->
                  <div class="rpc-item-header ng-hide" ng-show="item.lastResult != null">
                    <a href="#" ng-click="showLastResult(item)">
                      <div class="header-icon m-r-md" style="margin-right: 8px;">
                        <i class="pe page-header-icon pe-7s-plus"></i>
                      </div>
                      <div class="header-title m-l-md"><h5 class="rpc-item-text">Last Result</h5>
                      </div>
                    </a>
                  </div>

                  <div class="rpc-item-result-eth_getTransactionReceipt ng-hide"
                       ng-show="item.lastResult != null &amp;&amp; item.isLastResultVisible">
                    <pre class="panel panel-black-filled rpc-item-result ng-binding">null</pre>
                  </div>

                  <!-- Usage Sample -->
                  <div class="rpc-item-header flex-row flex-align-center rpc-usage">
                    <!--<a href="#" ng-click="showUsageHelp(item.methodName)">-->
                    <div class="header-icon m-l-none m-r-xs">
                      <i class="pe page-header-icon pe-7s-study"></i>
                    </div>
                    <pre class="panel panel-black-filled m-t-xs m-b-xs ng-binding">curl -X POST --data '{"jsonrpc":"2.0","method":"eth_getTransactionReceipt","params":["0xb903239f8543d04b5dc1ba6579132b143087c68db1b2168786408fcbce568238"],"id":1}' <span
                      class="ng-binding">http://localhost:8080/rpc</span></pre>
                    <!--<div class="header-title"><h5 class="rpc-item-text">Curl</h5>-->
                    <!--</div>-->
                    <!--</a>-->

                  </div>
                </div>
              </div>
            </il><!-- end ngRepeat: item in rpcItems | rpcItemFilter:filterWord -->
            <il ng-repeat="item in rpcItems | rpcItemFilter:filterWord" class="ng-scope">
              <div class="panel panel-dark-filled">
                <div class="panel-heading p-b-none p-t-none">
                  <div class="row">
                    <div class="col-sm-6">
                      <u><h4 class="font-weight-normal ng-binding">eth_getUncleByBlockHashAndIndex</h4></u>
                    </div>
                    <div class="col-sm-3">
                      <h5 class="font-weight-normal ng-binding ng-hide" ng-show="item.count > 0">Invoked: 0</h5>
                    </div>
                    <div class="col-sm-3 m-l-none">
                      <h5 class="font-weight-normal ng-binding ng-hide" ng-show="item.lastTime">Last call: </h5>
                    </div>
                  </div>
                </div>

                <div class="panel-footer p-b-none p-t-none">
                  <!-- Last Result -->
                  <div class="rpc-item-header ng-hide" ng-show="item.lastResult != null">
                    <a href="#" ng-click="showLastResult(item)">
                      <div class="header-icon m-r-md" style="margin-right: 8px;">
                        <i class="pe page-header-icon pe-7s-plus"></i>
                      </div>
                      <div class="header-title m-l-md"><h5 class="rpc-item-text">Last Result</h5>
                      </div>
                    </a>
                  </div>

                  <div class="rpc-item-result-eth_getUncleByBlockHashAndIndex ng-hide"
                       ng-show="item.lastResult != null &amp;&amp; item.isLastResultVisible">
                    <pre class="panel panel-black-filled rpc-item-result ng-binding">null</pre>
                  </div>

                  <!-- Usage Sample -->
                  <div class="rpc-item-header flex-row flex-align-center rpc-usage">
                    <!--<a href="#" ng-click="showUsageHelp(item.methodName)">-->
                    <div class="header-icon m-l-none m-r-xs">
                      <i class="pe page-header-icon pe-7s-study"></i>
                    </div>
                    <pre class="panel panel-black-filled m-t-xs m-b-xs ng-binding">curl -X POST --data '{"jsonrpc":"2.0","method":"eth_getUncleByBlockHashAndIndex","params":["0xc6ef2fc5426d6ad6fd9e2a26abeab0aa2411b7ab17f30a99d3cb96aed1d1055b", "0x0"],"id":1}' <span
                      class="ng-binding">http://localhost:8080/rpc</span></pre>
                    <!--<div class="header-title"><h5 class="rpc-item-text">Curl</h5>-->
                    <!--</div>-->
                    <!--</a>-->

                  </div>
                </div>
              </div>
            </il><!-- end ngRepeat: item in rpcItems | rpcItemFilter:filterWord -->
            <il ng-repeat="item in rpcItems | rpcItemFilter:filterWord" class="ng-scope">
              <div class="panel panel-dark-filled">
                <div class="panel-heading p-b-none p-t-none">
                  <div class="row">
                    <div class="col-sm-6">
                      <u><h4 class="font-weight-normal ng-binding">eth_getUncleByBlockNumberAndIndex</h4></u>
                    </div>
                    <div class="col-sm-3">
                      <h5 class="font-weight-normal ng-binding ng-hide" ng-show="item.count > 0">Invoked: 0</h5>
                    </div>
                    <div class="col-sm-3 m-l-none">
                      <h5 class="font-weight-normal ng-binding ng-hide" ng-show="item.lastTime">Last call: </h5>
                    </div>
                  </div>
                </div>

                <div class="panel-footer p-b-none p-t-none">
                  <!-- Last Result -->
                  <div class="rpc-item-header ng-hide" ng-show="item.lastResult != null">
                    <a href="#" ng-click="showLastResult(item)">
                      <div class="header-icon m-r-md" style="margin-right: 8px;">
                        <i class="pe page-header-icon pe-7s-plus"></i>
                      </div>
                      <div class="header-title m-l-md"><h5 class="rpc-item-text">Last Result</h5>
                      </div>
                    </a>
                  </div>

                  <div class="rpc-item-result-eth_getUncleByBlockNumberAndIndex ng-hide"
                       ng-show="item.lastResult != null &amp;&amp; item.isLastResultVisible">
                    <pre class="panel panel-black-filled rpc-item-result ng-binding">null</pre>
                  </div>

                  <!-- Usage Sample -->
                  <div class="rpc-item-header flex-row flex-align-center rpc-usage">
                    <!--<a href="#" ng-click="showUsageHelp(item.methodName)">-->
                    <div class="header-icon m-l-none m-r-xs">
                      <i class="pe page-header-icon pe-7s-study"></i>
                    </div>
                    <pre class="panel panel-black-filled m-t-xs m-b-xs ng-binding">curl -X POST --data '{"jsonrpc":"2.0","method":"eth_getUncleByBlockNumberAndIndex","params":["0x29c", "0x0"],"id":1}' <span
                      class="ng-binding">http://localhost:8080/rpc</span></pre>
                    <!--<div class="header-title"><h5 class="rpc-item-text">Curl</h5>-->
                    <!--</div>-->
                    <!--</a>-->

                  </div>
                </div>
              </div>
            </il><!-- end ngRepeat: item in rpcItems | rpcItemFilter:filterWord -->
            <il ng-repeat="item in rpcItems | rpcItemFilter:filterWord" class="ng-scope">
              <div class="panel panel-dark-filled">
                <div class="panel-heading p-b-none p-t-none">
                  <div class="row">
                    <div class="col-sm-6">
                      <u><h4 class="font-weight-normal ng-binding">eth_getUncleCountByBlockHash</h4></u>
                    </div>
                    <div class="col-sm-3">
                      <h5 class="font-weight-normal ng-binding ng-hide" ng-show="item.count > 0">Invoked: 0</h5>
                    </div>
                    <div class="col-sm-3 m-l-none">
                      <h5 class="font-weight-normal ng-binding ng-hide" ng-show="item.lastTime">Last call: </h5>
                    </div>
                  </div>
                </div>

                <div class="panel-footer p-b-none p-t-none">
                  <!-- Last Result -->
                  <div class="rpc-item-header ng-hide" ng-show="item.lastResult != null">
                    <a href="#" ng-click="showLastResult(item)">
                      <div class="header-icon m-r-md" style="margin-right: 8px;">
                        <i class="pe page-header-icon pe-7s-plus"></i>
                      </div>
                      <div class="header-title m-l-md"><h5 class="rpc-item-text">Last Result</h5>
                      </div>
                    </a>
                  </div>

                  <div class="rpc-item-result-eth_getUncleCountByBlockHash ng-hide"
                       ng-show="item.lastResult != null &amp;&amp; item.isLastResultVisible">
                    <pre class="panel panel-black-filled rpc-item-result ng-binding">null</pre>
                  </div>

                  <!-- Usage Sample -->
                  <div class="rpc-item-header flex-row flex-align-center rpc-usage">
                    <!--<a href="#" ng-click="showUsageHelp(item.methodName)">-->
                    <div class="header-icon m-l-none m-r-xs">
                      <i class="pe page-header-icon pe-7s-study"></i>
                    </div>
                    <pre class="panel panel-black-filled m-t-xs m-b-xs ng-binding">curl -X POST --data '{"jsonrpc":"2.0","method":"eth_getUncleCountByBlockHash","params":["0xb903239f8543d04b5dc1ba6579132b143087c68db1b2168786408fcbce568238"],"id"Block:1}' <span
                      class="ng-binding">http://localhost:8080/rpc</span></pre>
                    <!--<div class="header-title"><h5 class="rpc-item-text">Curl</h5>-->
                    <!--</div>-->
                    <!--</a>-->

                  </div>
                </div>
              </div>
            </il><!-- end ngRepeat: item in rpcItems | rpcItemFilter:filterWord -->
            <il ng-repeat="item in rpcItems | rpcItemFilter:filterWord" class="ng-scope">
              <div class="panel panel-dark-filled">
                <div class="panel-heading p-b-none p-t-none">
                  <div class="row">
                    <div class="col-sm-6">
                      <u><h4 class="font-weight-normal ng-binding">eth_getUncleCountByBlockNumber</h4></u>
                    </div>
                    <div class="col-sm-3">
                      <h5 class="font-weight-normal ng-binding ng-hide" ng-show="item.count > 0">Invoked: 0</h5>
                    </div>
                    <div class="col-sm-3 m-l-none">
                      <h5 class="font-weight-normal ng-binding ng-hide" ng-show="item.lastTime">Last call: </h5>
                    </div>
                  </div>
                </div>

                <div class="panel-footer p-b-none p-t-none">
                  <!-- Last Result -->
                  <div class="rpc-item-header ng-hide" ng-show="item.lastResult != null">
                    <a href="#" ng-click="showLastResult(item)">
                      <div class="header-icon m-r-md" style="margin-right: 8px;">
                        <i class="pe page-header-icon pe-7s-plus"></i>
                      </div>
                      <div class="header-title m-l-md"><h5 class="rpc-item-text">Last Result</h5>
                      </div>
                    </a>
                  </div>

                  <div class="rpc-item-result-eth_getUncleCountByBlockNumber ng-hide"
                       ng-show="item.lastResult != null &amp;&amp; item.isLastResultVisible">
                    <pre class="panel panel-black-filled rpc-item-result ng-binding">null</pre>
                  </div>

                  <!-- Usage Sample -->
                  <div class="rpc-item-header flex-row flex-align-center rpc-usage">
                    <!--<a href="#" ng-click="showUsageHelp(item.methodName)">-->
                    <div class="header-icon m-l-none m-r-xs">
                      <i class="pe page-header-icon pe-7s-study"></i>
                    </div>
                    <pre class="panel panel-black-filled m-t-xs m-b-xs ng-binding">curl -X POST --data '{"jsonrpc":"2.0","method":"eth_getUncleCountByBlockNumber","params":["0xe8"],"id":1}' <span
                      class="ng-binding">http://localhost:8080/rpc</span></pre>
                    <!--<div class="header-title"><h5 class="rpc-item-text">Curl</h5>-->
                    <!--</div>-->
                    <!--</a>-->

                  </div>
                </div>
              </div>
            </il><!-- end ngRepeat: item in rpcItems | rpcItemFilter:filterWord -->
            <il ng-repeat="item in rpcItems | rpcItemFilter:filterWord" class="ng-scope">
              <div class="panel panel-dark-filled">
                <div class="panel-heading p-b-none p-t-none">
                  <div class="row">
                    <div class="col-sm-6">
                      <u><h4 class="font-weight-normal ng-binding">eth_getWork</h4></u>
                    </div>
                    <div class="col-sm-3">
                      <h5 class="font-weight-normal ng-binding ng-hide" ng-show="item.count > 0">Invoked: 0</h5>
                    </div>
                    <div class="col-sm-3 m-l-none">
                      <h5 class="font-weight-normal ng-binding ng-hide" ng-show="item.lastTime">Last call: </h5>
                    </div>
                  </div>
                </div>

                <div class="panel-footer p-b-none p-t-none">
                  <!-- Last Result -->
                  <div class="rpc-item-header ng-hide" ng-show="item.lastResult != null">
                    <a href="#" ng-click="showLastResult(item)">
                      <div class="header-icon m-r-md" style="margin-right: 8px;">
                        <i class="pe page-header-icon pe-7s-plus"></i>
                      </div>
                      <div class="header-title m-l-md"><h5 class="rpc-item-text">Last Result</h5>
                      </div>
                    </a>
                  </div>

                  <div class="rpc-item-result-eth_getWork ng-hide"
                       ng-show="item.lastResult != null &amp;&amp; item.isLastResultVisible">
                    <pre class="panel panel-black-filled rpc-item-result ng-binding">null</pre>
                  </div>

                  <!-- Usage Sample -->
                  <div class="rpc-item-header flex-row flex-align-center rpc-usage">
                    <!--<a href="#" ng-click="showUsageHelp(item.methodName)">-->
                    <div class="header-icon m-l-none m-r-xs">
                      <i class="pe page-header-icon pe-7s-study"></i>
                    </div>
                    <pre class="panel panel-black-filled m-t-xs m-b-xs ng-binding">curl -X POST --data '{"jsonrpc":"2.0","method":"eth_getWork","params":[],"id":73}' <span
                      class="ng-binding">http://localhost:8080/rpc</span></pre>
                    <!--<div class="header-title"><h5 class="rpc-item-text">Curl</h5>-->
                    <!--</div>-->
                    <!--</a>-->

                  </div>
                </div>
              </div>
            </il><!-- end ngRepeat: item in rpcItems | rpcItemFilter:filterWord -->
            <il ng-repeat="item in rpcItems | rpcItemFilter:filterWord" class="ng-scope">
              <div class="panel panel-dark-filled">
                <div class="panel-heading p-b-none p-t-none">
                  <div class="row">
                    <div class="col-sm-6">
                      <u><h4 class="font-weight-normal ng-binding">eth_hashrate</h4></u>
                    </div>
                    <div class="col-sm-3">
                      <h5 class="font-weight-normal ng-binding ng-hide" ng-show="item.count > 0">Invoked: 0</h5>
                    </div>
                    <div class="col-sm-3 m-l-none">
                      <h5 class="font-weight-normal ng-binding ng-hide" ng-show="item.lastTime">Last call: </h5>
                    </div>
                  </div>
                </div>

                <div class="panel-footer p-b-none p-t-none">
                  <!-- Last Result -->
                  <div class="rpc-item-header ng-hide" ng-show="item.lastResult != null">
                    <a href="#" ng-click="showLastResult(item)">
                      <div class="header-icon m-r-md" style="margin-right: 8px;">
                        <i class="pe page-header-icon pe-7s-plus"></i>
                      </div>
                      <div class="header-title m-l-md"><h5 class="rpc-item-text">Last Result</h5>
                      </div>
                    </a>
                  </div>

                  <div class="rpc-item-result-eth_hashrate ng-hide"
                       ng-show="item.lastResult != null &amp;&amp; item.isLastResultVisible">
                    <pre class="panel panel-black-filled rpc-item-result ng-binding">null</pre>
                  </div>

                  <!-- Usage Sample -->
                  <div class="rpc-item-header flex-row flex-align-center rpc-usage">
                    <!--<a href="#" ng-click="showUsageHelp(item.methodName)">-->
                    <div class="header-icon m-l-none m-r-xs">
                      <i class="pe page-header-icon pe-7s-study"></i>
                    </div>
                    <pre class="panel panel-black-filled m-t-xs m-b-xs ng-binding">curl -X POST --data '{"jsonrpc":"2.0","method":"eth_hashrate","params":[],"id":71}' <span
                      class="ng-binding">http://localhost:8080/rpc</span></pre>
                    <!--<div class="header-title"><h5 class="rpc-item-text">Curl</h5>-->
                    <!--</div>-->
                    <!--</a>-->

                  </div>
                </div>
              </div>
            </il><!-- end ngRepeat: item in rpcItems | rpcItemFilter:filterWord -->
            <il ng-repeat="item in rpcItems | rpcItemFilter:filterWord" class="ng-scope">
              <div class="panel panel-dark-filled">
                <div class="panel-heading p-b-none p-t-none">
                  <div class="row">
                    <div class="col-sm-6">
                      <u><h4 class="font-weight-normal ng-binding">eth_mining</h4></u>
                    </div>
                    <div class="col-sm-3">
                      <h5 class="font-weight-normal ng-binding ng-hide" ng-show="item.count > 0">Invoked: 0</h5>
                    </div>
                    <div class="col-sm-3 m-l-none">
                      <h5 class="font-weight-normal ng-binding ng-hide" ng-show="item.lastTime">Last call: </h5>
                    </div>
                  </div>
                </div>

                <div class="panel-footer p-b-none p-t-none">
                  <!-- Last Result -->
                  <div class="rpc-item-header ng-hide" ng-show="item.lastResult != null">
                    <a href="#" ng-click="showLastResult(item)">
                      <div class="header-icon m-r-md" style="margin-right: 8px;">
                        <i class="pe page-header-icon pe-7s-plus"></i>
                      </div>
                      <div class="header-title m-l-md"><h5 class="rpc-item-text">Last Result</h5>
                      </div>
                    </a>
                  </div>

                  <div class="rpc-item-result-eth_mining ng-hide"
                       ng-show="item.lastResult != null &amp;&amp; item.isLastResultVisible">
                    <pre class="panel panel-black-filled rpc-item-result ng-binding">null</pre>
                  </div>

                  <!-- Usage Sample -->
                  <div class="rpc-item-header flex-row flex-align-center rpc-usage">
                    <!--<a href="#" ng-click="showUsageHelp(item.methodName)">-->
                    <div class="header-icon m-l-none m-r-xs">
                      <i class="pe page-header-icon pe-7s-study"></i>
                    </div>
                    <pre class="panel panel-black-filled m-t-xs m-b-xs ng-binding">curl -X POST --data '{"jsonrpc":"2.0","method":"eth_mining","params":[],"id":71}' <span
                      class="ng-binding">http://localhost:8080/rpc</span></pre>
                    <!--<div class="header-title"><h5 class="rpc-item-text">Curl</h5>-->
                    <!--</div>-->
                    <!--</a>-->

                  </div>
                </div>
              </div>
            </il><!-- end ngRepeat: item in rpcItems | rpcItemFilter:filterWord -->
            <il ng-repeat="item in rpcItems | rpcItemFilter:filterWord" class="ng-scope">
              <div class="panel panel-dark-filled">
                <div class="panel-heading p-b-none p-t-none">
                  <div class="row">
                    <div class="col-sm-6">
                      <u><h4 class="font-weight-normal ng-binding">eth_newBlockFilter</h4></u>
                    </div>
                    <div class="col-sm-3">
                      <h5 class="font-weight-normal ng-binding ng-hide" ng-show="item.count > 0">Invoked: 0</h5>
                    </div>
                    <div class="col-sm-3 m-l-none">
                      <h5 class="font-weight-normal ng-binding ng-hide" ng-show="item.lastTime">Last call: </h5>
                    </div>
                  </div>
                </div>

                <div class="panel-footer p-b-none p-t-none">
                  <!-- Last Result -->
                  <div class="rpc-item-header ng-hide" ng-show="item.lastResult != null">
                    <a href="#" ng-click="showLastResult(item)">
                      <div class="header-icon m-r-md" style="margin-right: 8px;">
                        <i class="pe page-header-icon pe-7s-plus"></i>
                      </div>
                      <div class="header-title m-l-md"><h5 class="rpc-item-text">Last Result</h5>
                      </div>
                    </a>
                  </div>

                  <div class="rpc-item-result-eth_newBlockFilter ng-hide"
                       ng-show="item.lastResult != null &amp;&amp; item.isLastResultVisible">
                    <pre class="panel panel-black-filled rpc-item-result ng-binding">null</pre>
                  </div>

                  <!-- Usage Sample -->
                  <div class="rpc-item-header flex-row flex-align-center rpc-usage">
                    <!--<a href="#" ng-click="showUsageHelp(item.methodName)">-->
                    <div class="header-icon m-l-none m-r-xs">
                      <i class="pe page-header-icon pe-7s-study"></i>
                    </div>
                    <pre class="panel panel-black-filled m-t-xs m-b-xs ng-binding">curl -X POST --data '{"jsonrpc":"2.0","method":"eth_newBlockFilter","params":[],"id":73}' <span
                      class="ng-binding">http://localhost:8080/rpc</span></pre>
                    <!--<div class="header-title"><h5 class="rpc-item-text">Curl</h5>-->
                    <!--</div>-->
                    <!--</a>-->

                  </div>
                </div>
              </div>
            </il><!-- end ngRepeat: item in rpcItems | rpcItemFilter:filterWord -->
            <il ng-repeat="item in rpcItems | rpcItemFilter:filterWord" class="ng-scope">
              <div class="panel panel-dark-filled">
                <div class="panel-heading p-b-none p-t-none">
                  <div class="row">
                    <div class="col-sm-6">
                      <u><h4 class="font-weight-normal ng-binding">eth_newFilter</h4></u>
                    </div>
                    <div class="col-sm-3">
                      <h5 class="font-weight-normal ng-binding ng-hide" ng-show="item.count > 0">Invoked: 0</h5>
                    </div>
                    <div class="col-sm-3 m-l-none">
                      <h5 class="font-weight-normal ng-binding ng-hide" ng-show="item.lastTime">Last call: </h5>
                    </div>
                  </div>
                </div>

                <div class="panel-footer p-b-none p-t-none">
                  <!-- Last Result -->
                  <div class="rpc-item-header ng-hide" ng-show="item.lastResult != null">
                    <a href="#" ng-click="showLastResult(item)">
                      <div class="header-icon m-r-md" style="margin-right: 8px;">
                        <i class="pe page-header-icon pe-7s-plus"></i>
                      </div>
                      <div class="header-title m-l-md"><h5 class="rpc-item-text">Last Result</h5>
                      </div>
                    </a>
                  </div>

                  <div class="rpc-item-result-eth_newFilter ng-hide"
                       ng-show="item.lastResult != null &amp;&amp; item.isLastResultVisible">
                    <pre class="panel panel-black-filled rpc-item-result ng-binding">null</pre>
                  </div>

                  <!-- Usage Sample -->
                  <div class="rpc-item-header flex-row flex-align-center rpc-usage">
                    <!--<a href="#" ng-click="showUsageHelp(item.methodName)">-->
                    <div class="header-icon m-l-none m-r-xs">
                      <i class="pe page-header-icon pe-7s-study"></i>
                    </div>
                    <pre class="panel panel-black-filled m-t-xs m-b-xs ng-binding">curl -X POST --data '{"jsonrpc":"2.0","method":"eth_newFilter","params":[{"topics":["0x12341234"]}],"id":73}' <span
                      class="ng-binding">http://localhost:8080/rpc</span></pre>
                    <!--<div class="header-title"><h5 class="rpc-item-text">Curl</h5>-->
                    <!--</div>-->
                    <!--</a>-->

                  </div>
                </div>
              </div>
            </il><!-- end ngRepeat: item in rpcItems | rpcItemFilter:filterWord -->
            <il ng-repeat="item in rpcItems | rpcItemFilter:filterWord" class="ng-scope">
              <div class="panel panel-dark-filled">
                <div class="panel-heading p-b-none p-t-none">
                  <div class="row">
                    <div class="col-sm-6">
                      <u><h4 class="font-weight-normal ng-binding">eth_newPendingTransactionFilter</h4></u>
                    </div>
                    <div class="col-sm-3">
                      <h5 class="font-weight-normal ng-binding ng-hide" ng-show="item.count > 0">Invoked: 0</h5>
                    </div>
                    <div class="col-sm-3 m-l-none">
                      <h5 class="font-weight-normal ng-binding ng-hide" ng-show="item.lastTime">Last call: </h5>
                    </div>
                  </div>
                </div>

                <div class="panel-footer p-b-none p-t-none">
                  <!-- Last Result -->
                  <div class="rpc-item-header ng-hide" ng-show="item.lastResult != null">
                    <a href="#" ng-click="showLastResult(item)">
                      <div class="header-icon m-r-md" style="margin-right: 8px;">
                        <i class="pe page-header-icon pe-7s-plus"></i>
                      </div>
                      <div class="header-title m-l-md"><h5 class="rpc-item-text">Last Result</h5>
                      </div>
                    </a>
                  </div>

                  <div class="rpc-item-result-eth_newPendingTransactionFilter ng-hide"
                       ng-show="item.lastResult != null &amp;&amp; item.isLastResultVisible">
                    <pre class="panel panel-black-filled rpc-item-result ng-binding">null</pre>
                  </div>

                  <!-- Usage Sample -->
                  <div class="rpc-item-header flex-row flex-align-center rpc-usage">
                    <!--<a href="#" ng-click="showUsageHelp(item.methodName)">-->
                    <div class="header-icon m-l-none m-r-xs">
                      <i class="pe page-header-icon pe-7s-study"></i>
                    </div>
                    <pre class="panel panel-black-filled m-t-xs m-b-xs ng-binding">curl -X POST --data '{"jsonrpc":"2.0","method":"eth_newPendingTransactionFilter","params":[],"id":73}' <span
                      class="ng-binding">http://localhost:8080/rpc</span></pre>
                    <!--<div class="header-title"><h5 class="rpc-item-text">Curl</h5>-->
                    <!--</div>-->
                    <!--</a>-->

                  </div>
                </div>
              </div>
            </il><!-- end ngRepeat: item in rpcItems | rpcItemFilter:filterWord -->
            <il ng-repeat="item in rpcItems | rpcItemFilter:filterWord" class="ng-scope">
              <div class="panel panel-dark-filled">
                <div class="panel-heading p-b-none p-t-none">
                  <div class="row">
                    <div class="col-sm-6">
                      <u><h4 class="font-weight-normal ng-binding">eth_protocolVersion</h4></u>
                    </div>
                    <div class="col-sm-3">
                      <h5 class="font-weight-normal ng-binding ng-hide" ng-show="item.count > 0">Invoked: 0</h5>
                    </div>
                    <div class="col-sm-3 m-l-none">
                      <h5 class="font-weight-normal ng-binding ng-hide" ng-show="item.lastTime">Last call: </h5>
                    </div>
                  </div>
                </div>

                <div class="panel-footer p-b-none p-t-none">
                  <!-- Last Result -->
                  <div class="rpc-item-header ng-hide" ng-show="item.lastResult != null">
                    <a href="#" ng-click="showLastResult(item)">
                      <div class="header-icon m-r-md" style="margin-right: 8px;">
                        <i class="pe page-header-icon pe-7s-plus"></i>
                      </div>
                      <div class="header-title m-l-md"><h5 class="rpc-item-text">Last Result</h5>
                      </div>
                    </a>
                  </div>

                  <div class="rpc-item-result-eth_protocolVersion ng-hide"
                       ng-show="item.lastResult != null &amp;&amp; item.isLastResultVisible">
                    <pre class="panel panel-black-filled rpc-item-result ng-binding">null</pre>
                  </div>

                  <!-- Usage Sample -->
                  <div class="rpc-item-header flex-row flex-align-center rpc-usage">
                    <!--<a href="#" ng-click="showUsageHelp(item.methodName)">-->
                    <div class="header-icon m-l-none m-r-xs">
                      <i class="pe page-header-icon pe-7s-study"></i>
                    </div>
                    <pre class="panel panel-black-filled m-t-xs m-b-xs ng-binding">curl -X POST --data '{"jsonrpc":"2.0","method":"eth_protocolVersion","params":[],"id":67}' <span
                      class="ng-binding">http://localhost:8080/rpc</span></pre>
                    <!--<div class="header-title"><h5 class="rpc-item-text">Curl</h5>-->
                    <!--</div>-->
                    <!--</a>-->

                  </div>
                </div>
              </div>
            </il><!-- end ngRepeat: item in rpcItems | rpcItemFilter:filterWord -->
            <il ng-repeat="item in rpcItems | rpcItemFilter:filterWord" class="ng-scope">
              <div class="panel panel-dark-filled">
                <div class="panel-heading p-b-none p-t-none">
                  <div class="row">
                    <div class="col-sm-6">
                      <u><h4 class="font-weight-normal ng-binding">eth_sendRawTransaction</h4></u>
                    </div>
                    <div class="col-sm-3">
                      <h5 class="font-weight-normal ng-binding ng-hide" ng-show="item.count > 0">Invoked: 0</h5>
                    </div>
                    <div class="col-sm-3 m-l-none">
                      <h5 class="font-weight-normal ng-binding ng-hide" ng-show="item.lastTime">Last call: </h5>
                    </div>
                  </div>
                </div>

                <div class="panel-footer p-b-none p-t-none">
                  <!-- Last Result -->
                  <div class="rpc-item-header ng-hide" ng-show="item.lastResult != null">
                    <a href="#" ng-click="showLastResult(item)">
                      <div class="header-icon m-r-md" style="margin-right: 8px;">
                        <i class="pe page-header-icon pe-7s-plus"></i>
                      </div>
                      <div class="header-title m-l-md"><h5 class="rpc-item-text">Last Result</h5>
                      </div>
                    </a>
                  </div>

                  <div class="rpc-item-result-eth_sendRawTransaction ng-hide"
                       ng-show="item.lastResult != null &amp;&amp; item.isLastResultVisible">
                    <pre class="panel panel-black-filled rpc-item-result ng-binding">null</pre>
                  </div>

                  <!-- Usage Sample -->
                  <div class="rpc-item-header flex-row flex-align-center rpc-usage">
                    <!--<a href="#" ng-click="showUsageHelp(item.methodName)">-->
                    <div class="header-icon m-l-none m-r-xs">
                      <i class="pe page-header-icon pe-7s-study"></i>
                    </div>
                    <pre class="panel panel-black-filled m-t-xs m-b-xs ng-binding">curl -X POST --data '{"jsonrpc":"2.0","method":"eth_sendRawTransaction","params":[{"from":"0xcd2a3d9f938e13cd947ec05abc7fe734df8dd826", "to":"0x79b08ad8787060333663d19704909ee7b1903e58", "gas":"0x300000", "gasPrice":"0x10000000000", "value":"0x7777", "data":"0x", "nounce":"0x101F15"}],"id":1}' <span
                      class="ng-binding">http://localhost:8080/rpc</span></pre>
                    <!--<div class="header-title"><h5 class="rpc-item-text">Curl</h5>-->
                    <!--</div>-->
                    <!--</a>-->

                  </div>
                </div>
              </div>
            </il><!-- end ngRepeat: item in rpcItems | rpcItemFilter:filterWord -->
            <il ng-repeat="item in rpcItems | rpcItemFilter:filterWord" class="ng-scope">
              <div class="panel panel-dark-filled">
                <div class="panel-heading p-b-none p-t-none">
                  <div class="row">
                    <div class="col-sm-6">
                      <u><h4 class="font-weight-normal ng-binding">eth_sendTransaction</h4></u>
                    </div>
                    <div class="col-sm-3">
                      <h5 class="font-weight-normal ng-binding ng-hide" ng-show="item.count > 0">Invoked: 0</h5>
                    </div>
                    <div class="col-sm-3 m-l-none">
                      <h5 class="font-weight-normal ng-binding ng-hide" ng-show="item.lastTime">Last call: </h5>
                    </div>
                  </div>
                </div>

                <div class="panel-footer p-b-none p-t-none">
                  <!-- Last Result -->
                  <div class="rpc-item-header ng-hide" ng-show="item.lastResult != null">
                    <a href="#" ng-click="showLastResult(item)">
                      <div class="header-icon m-r-md" style="margin-right: 8px;">
                        <i class="pe page-header-icon pe-7s-plus"></i>
                      </div>
                      <div class="header-title m-l-md"><h5 class="rpc-item-text">Last Result</h5>
                      </div>
                    </a>
                  </div>

                  <div class="rpc-item-result-eth_sendTransaction ng-hide"
                       ng-show="item.lastResult != null &amp;&amp; item.isLastResultVisible">
                    <pre class="panel panel-black-filled rpc-item-result ng-binding">null</pre>
                  </div>

                  <!-- Usage Sample -->
                  <div class="rpc-item-header flex-row flex-align-center rpc-usage">
                    <!--<a href="#" ng-click="showUsageHelp(item.methodName)">-->
                    <div class="header-icon m-l-none m-r-xs">
                      <i class="pe page-header-icon pe-7s-study"></i>
                    </div>
                    <pre class="panel panel-black-filled m-t-xs m-b-xs ng-binding">curl -X POST --data '{"jsonrpc":"2.0","method":"eth_sendTransaction","params":[{"from":"0xcd2a3d9f938e13cd947ec05abc7fe734df8dd826", "to":"0x79b08ad8787060333663d19704909ee7b1903e58", "gas":"0x300000", "gasPrice":"0x10000000000", "value":"0x7777", "data":"0x", "nounce":"0x101F15"}],"id":1}' <span
                      class="ng-binding">http://localhost:8080/rpc</span></pre>
                    <!--<div class="header-title"><h5 class="rpc-item-text">Curl</h5>-->
                    <!--</div>-->
                    <!--</a>-->

                  </div>
                </div>
              </div>
            </il><!-- end ngRepeat: item in rpcItems | rpcItemFilter:filterWord -->
            <il ng-repeat="item in rpcItems | rpcItemFilter:filterWord" class="ng-scope">
              <div class="panel panel-dark-filled">
                <div class="panel-heading p-b-none p-t-none">
                  <div class="row">
                    <div class="col-sm-6">
                      <u><h4 class="font-weight-normal ng-binding">eth_sign</h4></u>
                    </div>
                    <div class="col-sm-3">
                      <h5 class="font-weight-normal ng-binding ng-hide" ng-show="item.count > 0">Invoked: 0</h5>
                    </div>
                    <div class="col-sm-3 m-l-none">
                      <h5 class="font-weight-normal ng-binding ng-hide" ng-show="item.lastTime">Last call: </h5>
                    </div>
                  </div>
                </div>

                <div class="panel-footer p-b-none p-t-none">
                  <!-- Last Result -->
                  <div class="rpc-item-header ng-hide" ng-show="item.lastResult != null">
                    <a href="#" ng-click="showLastResult(item)">
                      <div class="header-icon m-r-md" style="margin-right: 8px;">
                        <i class="pe page-header-icon pe-7s-plus"></i>
                      </div>
                      <div class="header-title m-l-md"><h5 class="rpc-item-text">Last Result</h5>
                      </div>
                    </a>
                  </div>

                  <div class="rpc-item-result-eth_sign ng-hide"
                       ng-show="item.lastResult != null &amp;&amp; item.isLastResultVisible">
                    <pre class="panel panel-black-filled rpc-item-result ng-binding">null</pre>
                  </div>

                  <!-- Usage Sample -->
                  <div class="rpc-item-header flex-row flex-align-center rpc-usage">
                    <!--<a href="#" ng-click="showUsageHelp(item.methodName)">-->
                    <div class="header-icon m-l-none m-r-xs">
                      <i class="pe page-header-icon pe-7s-study"></i>
                    </div>
                    <pre class="panel panel-black-filled m-t-xs m-b-xs ng-binding">curl -X POST --data '{"jsonrpc":"2.0","method":"eth_sign","params":["0x8a3106a3e50576d4b6794a0e74d3bb5f8c9acaab", "0xc5d2460186f7233c927e7db2dcc703c0e500b653ca82273b7bfad8045d85a470"],"id":1}' <span
                      class="ng-binding">http://localhost:8080/rpc</span></pre>
                    <!--<div class="header-title"><h5 class="rpc-item-text">Curl</h5>-->
                    <!--</div>-->
                    <!--</a>-->

                  </div>
                </div>
              </div>
            </il><!-- end ngRepeat: item in rpcItems | rpcItemFilter:filterWord -->
            <il ng-repeat="item in rpcItems | rpcItemFilter:filterWord" class="ng-scope">
              <div class="panel panel-dark-filled">
                <div class="panel-heading p-b-none p-t-none">
                  <div class="row">
                    <div class="col-sm-6">
                      <u><h4 class="font-weight-normal ng-binding">eth_submitHashrate</h4></u>
                    </div>
                    <div class="col-sm-3">
                      <h5 class="font-weight-normal ng-binding ng-hide" ng-show="item.count > 0">Invoked: 0</h5>
                    </div>
                    <div class="col-sm-3 m-l-none">
                      <h5 class="font-weight-normal ng-binding ng-hide" ng-show="item.lastTime">Last call: </h5>
                    </div>
                  </div>
                </div>

                <div class="panel-footer p-b-none p-t-none">
                  <!-- Last Result -->
                  <div class="rpc-item-header ng-hide" ng-show="item.lastResult != null">
                    <a href="#" ng-click="showLastResult(item)">
                      <div class="header-icon m-r-md" style="margin-right: 8px;">
                        <i class="pe page-header-icon pe-7s-plus"></i>
                      </div>
                      <div class="header-title m-l-md"><h5 class="rpc-item-text">Last Result</h5>
                      </div>
                    </a>
                  </div>

                  <div class="rpc-item-result-eth_submitHashrate ng-hide"
                       ng-show="item.lastResult != null &amp;&amp; item.isLastResultVisible">
                    <pre class="panel panel-black-filled rpc-item-result ng-binding">null</pre>
                  </div>

                  <!-- Usage Sample -->
                  <div class="rpc-item-header flex-row flex-align-center rpc-usage">
                    <!--<a href="#" ng-click="showUsageHelp(item.methodName)">-->
                    <div class="header-icon m-l-none m-r-xs">
                      <i class="pe page-header-icon pe-7s-study"></i>
                    </div>
                    <pre class="panel panel-black-filled m-t-xs m-b-xs ng-binding">curl -X POST --data '{"jsonrpc":"2.0", "method":"eth_submitHashrate", "params":["0x0000000000000000000000000000000000000000000000000000000000500000", "0x59daa26581d0acd1fce254fb7e85952f4c09d0915afd33d3886cd914bc7d283c"],"id":73}' <span
                      class="ng-binding">http://localhost:8080/rpc</span></pre>
                    <!--<div class="header-title"><h5 class="rpc-item-text">Curl</h5>-->
                    <!--</div>-->
                    <!--</a>-->

                  </div>
                </div>
              </div>
            </il><!-- end ngRepeat: item in rpcItems | rpcItemFilter:filterWord -->
            <il ng-repeat="item in rpcItems | rpcItemFilter:filterWord" class="ng-scope">
              <div class="panel panel-dark-filled">
                <div class="panel-heading p-b-none p-t-none">
                  <div class="row">
                    <div class="col-sm-6">
                      <u><h4 class="font-weight-normal ng-binding">eth_submitWork</h4></u>
                    </div>
                    <div class="col-sm-3">
                      <h5 class="font-weight-normal ng-binding ng-hide" ng-show="item.count > 0">Invoked: 0</h5>
                    </div>
                    <div class="col-sm-3 m-l-none">
                      <h5 class="font-weight-normal ng-binding ng-hide" ng-show="item.lastTime">Last call: </h5>
                    </div>
                  </div>
                </div>

                <div class="panel-footer p-b-none p-t-none">
                  <!-- Last Result -->
                  <div class="rpc-item-header ng-hide" ng-show="item.lastResult != null">
                    <a href="#" ng-click="showLastResult(item)">
                      <div class="header-icon m-r-md" style="margin-right: 8px;">
                        <i class="pe page-header-icon pe-7s-plus"></i>
                      </div>
                      <div class="header-title m-l-md"><h5 class="rpc-item-text">Last Result</h5>
                      </div>
                    </a>
                  </div>

                  <div class="rpc-item-result-eth_submitWork ng-hide"
                       ng-show="item.lastResult != null &amp;&amp; item.isLastResultVisible">
                    <pre class="panel panel-black-filled rpc-item-result ng-binding">null</pre>
                  </div>

                  <!-- Usage Sample -->
                  <div class="rpc-item-header flex-row flex-align-center rpc-usage">
                    <!--<a href="#" ng-click="showUsageHelp(item.methodName)">-->
                    <div class="header-icon m-l-none m-r-xs">
                      <i class="pe page-header-icon pe-7s-study"></i>
                    </div>
                    <pre class="panel panel-black-filled m-t-xs m-b-xs ng-binding">curl -X POST --data '{"jsonrpc":"2.0", "method":"eth_submitWork", "params":["0x0000000000000001", "0x1234567890abcdef1234567890abcdef1234567890abcdef1234567890abcdef", "0xD1GE5700000000000000000000000000D1GE5700000000000000000000000000"],"id":73}' <span
                      class="ng-binding">http://localhost:8080/rpc</span></pre>
                    <!--<div class="header-title"><h5 class="rpc-item-text">Curl</h5>-->
                    <!--</div>-->
                    <!--</a>-->

                  </div>
                </div>
              </div>
            </il><!-- end ngRepeat: item in rpcItems | rpcItemFilter:filterWord -->
            <il ng-repeat="item in rpcItems | rpcItemFilter:filterWord" class="ng-scope">
              <div class="panel panel-dark-filled">
                <div class="panel-heading p-b-none p-t-none">
                  <div class="row">
                    <div class="col-sm-6">
                      <u><h4 class="font-weight-normal ng-binding">eth_syncing</h4></u>
                    </div>
                    <div class="col-sm-3">
                      <h5 class="font-weight-normal ng-binding ng-hide" ng-show="item.count > 0">Invoked: 0</h5>
                    </div>
                    <div class="col-sm-3 m-l-none">
                      <h5 class="font-weight-normal ng-binding ng-hide" ng-show="item.lastTime">Last call: </h5>
                    </div>
                  </div>
                </div>

                <div class="panel-footer p-b-none p-t-none">
                  <!-- Last Result -->
                  <div class="rpc-item-header ng-hide" ng-show="item.lastResult != null">
                    <a href="#" ng-click="showLastResult(item)">
                      <div class="header-icon m-r-md" style="margin-right: 8px;">
                        <i class="pe page-header-icon pe-7s-plus"></i>
                      </div>
                      <div class="header-title m-l-md"><h5 class="rpc-item-text">Last Result</h5>
                      </div>
                    </a>
                  </div>

                  <div class="rpc-item-result-eth_syncing ng-hide"
                       ng-show="item.lastResult != null &amp;&amp; item.isLastResultVisible">
                    <pre class="panel panel-black-filled rpc-item-result ng-binding">null</pre>
                  </div>

                  <!-- Usage Sample -->
                  <div class="rpc-item-header flex-row flex-align-center rpc-usage">
                    <!--<a href="#" ng-click="showUsageHelp(item.methodName)">-->
                    <div class="header-icon m-l-none m-r-xs">
                      <i class="pe page-header-icon pe-7s-study"></i>
                    </div>
                    <pre class="panel panel-black-filled m-t-xs m-b-xs ng-binding">curl -X POST --data '{"jsonrpc":"2.0","method":"eth_syncing","params":[],"id":1}' <span
                      class="ng-binding">http://localhost:8080/rpc</span></pre>
                    <!--<div class="header-title"><h5 class="rpc-item-text">Curl</h5>-->
                    <!--</div>-->
                    <!--</a>-->

                  </div>
                </div>
              </div>
            </il><!-- end ngRepeat: item in rpcItems | rpcItemFilter:filterWord -->
            <il ng-repeat="item in rpcItems | rpcItemFilter:filterWord" class="ng-scope">
              <div class="panel panel-dark-filled">
                <div class="panel-heading p-b-none p-t-none">
                  <div class="row">
                    <div class="col-sm-6">
                      <u><h4 class="font-weight-normal ng-binding">eth_uninstallFilter</h4></u>
                    </div>
                    <div class="col-sm-3">
                      <h5 class="font-weight-normal ng-binding ng-hide" ng-show="item.count > 0">Invoked: 0</h5>
                    </div>
                    <div class="col-sm-3 m-l-none">
                      <h5 class="font-weight-normal ng-binding ng-hide" ng-show="item.lastTime">Last call: </h5>
                    </div>
                  </div>
                </div>

                <div class="panel-footer p-b-none p-t-none">
                  <!-- Last Result -->
                  <div class="rpc-item-header ng-hide" ng-show="item.lastResult != null">
                    <a href="#" ng-click="showLastResult(item)">
                      <div class="header-icon m-r-md" style="margin-right: 8px;">
                        <i class="pe page-header-icon pe-7s-plus"></i>
                      </div>
                      <div class="header-title m-l-md"><h5 class="rpc-item-text">Last Result</h5>
                      </div>
                    </a>
                  </div>

                  <div class="rpc-item-result-eth_uninstallFilter ng-hide"
                       ng-show="item.lastResult != null &amp;&amp; item.isLastResultVisible">
                    <pre class="panel panel-black-filled rpc-item-result ng-binding">null</pre>
                  </div>

                  <!-- Usage Sample -->
                  <div class="rpc-item-header flex-row flex-align-center rpc-usage">
                    <!--<a href="#" ng-click="showUsageHelp(item.methodName)">-->
                    <div class="header-icon m-l-none m-r-xs">
                      <i class="pe page-header-icon pe-7s-study"></i>
                    </div>
                    <pre class="panel panel-black-filled m-t-xs m-b-xs ng-binding">curl -X POST --data '{"jsonrpc":"2.0","method":"eth_uninstallFilter","params":["0xb"],"id":73}' <span
                      class="ng-binding">http://localhost:8080/rpc</span></pre>
                    <!--<div class="header-title"><h5 class="rpc-item-text">Curl</h5>-->
                    <!--</div>-->
                    <!--</a>-->

                  </div>
                </div>
              </div>
            </il><!-- end ngRepeat: item in rpcItems | rpcItemFilter:filterWord -->
            <il ng-repeat="item in rpcItems | rpcItemFilter:filterWord" class="ng-scope">
              <div class="panel panel-dark-filled">
                <div class="panel-heading p-b-none p-t-none">
                  <div class="row">
                    <div class="col-sm-6">
                      <u><h4 class="font-weight-normal ng-binding">ethj_getTransactionReceipt</h4></u>
                    </div>
                    <div class="col-sm-3">
                      <h5 class="font-weight-normal ng-binding ng-hide" ng-show="item.count > 0">Invoked: 0</h5>
                    </div>
                    <div class="col-sm-3 m-l-none">
                      <h5 class="font-weight-normal ng-binding ng-hide" ng-show="item.lastTime">Last call: </h5>
                    </div>
                  </div>
                </div>

                <div class="panel-footer p-b-none p-t-none">
                  <!-- Last Result -->
                  <div class="rpc-item-header ng-hide" ng-show="item.lastResult != null">
                    <a href="#" ng-click="showLastResult(item)">
                      <div class="header-icon m-r-md" style="margin-right: 8px;">
                        <i class="pe page-header-icon pe-7s-plus"></i>
                      </div>
                      <div class="header-title m-l-md"><h5 class="rpc-item-text">Last Result</h5>
                      </div>
                    </a>
                  </div>

                  <div class="rpc-item-result-ethj_getTransactionReceipt ng-hide"
                       ng-show="item.lastResult != null &amp;&amp; item.isLastResultVisible">
                    <pre class="panel panel-black-filled rpc-item-result ng-binding">null</pre>
                  </div>

                  <!-- Usage Sample -->
                  <div class="rpc-item-header flex-row flex-align-center rpc-usage">
                    <!--<a href="#" ng-click="showUsageHelp(item.methodName)">-->
                    <div class="header-icon m-l-none m-r-xs">
                      <i class="pe page-header-icon pe-7s-study"></i>
                    </div>
                    <pre class="panel panel-black-filled m-t-xs m-b-xs ng-binding">curl -X POST --data '{"jsonrpc":"2.0","method":"ethj_getTransactionReceipt","params":["0x0"],"id":64}' <span
                      class="ng-binding">http://localhost:8080/rpc</span></pre>
                    <!--<div class="header-title"><h5 class="rpc-item-text">Curl</h5>-->
                    <!--</div>-->
                    <!--</a>-->

                  </div>
                </div>
              </div>
            </il><!-- end ngRepeat: item in rpcItems | rpcItemFilter:filterWord -->
            <il ng-repeat="item in rpcItems | rpcItemFilter:filterWord" class="ng-scope">
              <div class="panel panel-dark-filled">
                <div class="panel-heading p-b-none p-t-none">
                  <div class="row">
                    <div class="col-sm-6">
                      <u><h4 class="font-weight-normal ng-binding">ethj_listAvailableMethods</h4></u>
                    </div>
                    <div class="col-sm-3">
                      <h5 class="font-weight-normal ng-binding ng-hide" ng-show="item.count > 0">Invoked: 0</h5>
                    </div>
                    <div class="col-sm-3 m-l-none">
                      <h5 class="font-weight-normal ng-binding ng-hide" ng-show="item.lastTime">Last call: </h5>
                    </div>
                  </div>
                </div>

                <div class="panel-footer p-b-none p-t-none">
                  <!-- Last Result -->
                  <div class="rpc-item-header ng-hide" ng-show="item.lastResult != null">
                    <a href="#" ng-click="showLastResult(item)">
                      <div class="header-icon m-r-md" style="margin-right: 8px;">
                        <i class="pe page-header-icon pe-7s-plus"></i>
                      </div>
                      <div class="header-title m-l-md"><h5 class="rpc-item-text">Last Result</h5>
                      </div>
                    </a>
                  </div>

                  <div class="rpc-item-result-ethj_listAvailableMethods ng-hide"
                       ng-show="item.lastResult != null &amp;&amp; item.isLastResultVisible">
                    <pre class="panel panel-black-filled rpc-item-result ng-binding">null</pre>
                  </div>

                  <!-- Usage Sample -->
                  <div class="rpc-item-header flex-row flex-align-center rpc-usage">
                    <!--<a href="#" ng-click="showUsageHelp(item.methodName)">-->
                    <div class="header-icon m-l-none m-r-xs">
                      <i class="pe page-header-icon pe-7s-study"></i>
                    </div>
                    <pre class="panel panel-black-filled m-t-xs m-b-xs ng-binding">curl -X POST --data '{"jsonrpc":"2.0","method":"ethj_listAvailableMethods","params":[],"id":64}' <span
                      class="ng-binding">http://localhost:8080/rpc</span></pre>
                    <!--<div class="header-title"><h5 class="rpc-item-text">Curl</h5>-->
                    <!--</div>-->
                    <!--</a>-->

                  </div>
                </div>
              </div>
            </il><!-- end ngRepeat: item in rpcItems | rpcItemFilter:filterWord -->
            <il ng-repeat="item in rpcItems | rpcItemFilter:filterWord" class="ng-scope">
              <div class="panel panel-dark-filled">
                <div class="panel-heading p-b-none p-t-none">
                  <div class="row">
                    <div class="col-sm-6">
                      <u><h4 class="font-weight-normal ng-binding">miner_setEtherbase</h4></u>
                    </div>
                    <div class="col-sm-3">
                      <h5 class="font-weight-normal ng-binding ng-hide" ng-show="item.count > 0">Invoked: 0</h5>
                    </div>
                    <div class="col-sm-3 m-l-none">
                      <h5 class="font-weight-normal ng-binding ng-hide" ng-show="item.lastTime">Last call: </h5>
                    </div>
                  </div>
                </div>

                <div class="panel-footer p-b-none p-t-none">
                  <!-- Last Result -->
                  <div class="rpc-item-header ng-hide" ng-show="item.lastResult != null">
                    <a href="#" ng-click="showLastResult(item)">
                      <div class="header-icon m-r-md" style="margin-right: 8px;">
                        <i class="pe page-header-icon pe-7s-plus"></i>
                      </div>
                      <div class="header-title m-l-md"><h5 class="rpc-item-text">Last Result</h5>
                      </div>
                    </a>
                  </div>

                  <div class="rpc-item-result-miner_setEtherbase ng-hide"
                       ng-show="item.lastResult != null &amp;&amp; item.isLastResultVisible">
                    <pre class="panel panel-black-filled rpc-item-result ng-binding">null</pre>
                  </div>

                  <!-- Usage Sample -->
                  <div class="rpc-item-header flex-row flex-align-center rpc-usage">
                    <!--<a href="#" ng-click="showUsageHelp(item.methodName)">-->
                    <div class="header-icon m-l-none m-r-xs">
                      <i class="pe page-header-icon pe-7s-study"></i>
                    </div>
                    <pre class="panel panel-black-filled m-t-xs m-b-xs ng-binding">curl -X POST --data '{"jsonrpc":"2.0","method":"miner_setEtherbase","params":["0xcd2a3d9f938e13cd947ec05abc7fe734df8dd826"],"id":1}' <span
                      class="ng-binding">http://localhost:8080/rpc</span></pre>
                    <!--<div class="header-title"><h5 class="rpc-item-text">Curl</h5>-->
                    <!--</div>-->
                    <!--</a>-->

                  </div>
                </div>
              </div>
            </il><!-- end ngRepeat: item in rpcItems | rpcItemFilter:filterWord -->
            <il ng-repeat="item in rpcItems | rpcItemFilter:filterWord" class="ng-scope">
              <div class="panel panel-dark-filled">
                <div class="panel-heading p-b-none p-t-none">
                  <div class="row">
                    <div class="col-sm-6">
                      <u><h4 class="font-weight-normal ng-binding">miner_setExtra</h4></u>
                    </div>
                    <div class="col-sm-3">
                      <h5 class="font-weight-normal ng-binding ng-hide" ng-show="item.count > 0">Invoked: 0</h5>
                    </div>
                    <div class="col-sm-3 m-l-none">
                      <h5 class="font-weight-normal ng-binding ng-hide" ng-show="item.lastTime">Last call: </h5>
                    </div>
                  </div>
                </div>

                <div class="panel-footer p-b-none p-t-none">
                  <!-- Last Result -->
                  <div class="rpc-item-header ng-hide" ng-show="item.lastResult != null">
                    <a href="#" ng-click="showLastResult(item)">
                      <div class="header-icon m-r-md" style="margin-right: 8px;">
                        <i class="pe page-header-icon pe-7s-plus"></i>
                      </div>
                      <div class="header-title m-l-md"><h5 class="rpc-item-text">Last Result</h5>
                      </div>
                    </a>
                  </div>

                  <div class="rpc-item-result-miner_setExtra ng-hide"
                       ng-show="item.lastResult != null &amp;&amp; item.isLastResultVisible">
                    <pre class="panel panel-black-filled rpc-item-result ng-binding">null</pre>
                  </div>

                  <!-- Usage Sample -->
                  <div class="rpc-item-header flex-row flex-align-center rpc-usage">
                    <!--<a href="#" ng-click="showUsageHelp(item.methodName)">-->
                    <div class="header-icon m-l-none m-r-xs">
                      <i class="pe page-header-icon pe-7s-study"></i>
                    </div>
                    <pre class="panel panel-black-filled m-t-xs m-b-xs ng-binding">curl -X POST --data '{"jsonrpc":"2.0","method":"miner_setExtra","params":["0x457468657265756d204861726d6f6e79"],"id":1}' <span
                      class="ng-binding">http://localhost:8080/rpc</span></pre>
                    <!--<div class="header-title"><h5 class="rpc-item-text">Curl</h5>-->
                    <!--</div>-->
                    <!--</a>-->

                  </div>
                </div>
              </div>
            </il><!-- end ngRepeat: item in rpcItems | rpcItemFilter:filterWord -->
            <il ng-repeat="item in rpcItems | rpcItemFilter:filterWord" class="ng-scope">
              <div class="panel panel-dark-filled">
                <div class="panel-heading p-b-none p-t-none">
                  <div class="row">
                    <div class="col-sm-6">
                      <u><h4 class="font-weight-normal ng-binding">miner_setGasPrice</h4></u>
                    </div>
                    <div class="col-sm-3">
                      <h5 class="font-weight-normal ng-binding ng-hide" ng-show="item.count > 0">Invoked: 0</h5>
                    </div>
                    <div class="col-sm-3 m-l-none">
                      <h5 class="font-weight-normal ng-binding ng-hide" ng-show="item.lastTime">Last call: </h5>
                    </div>
                  </div>
                </div>

                <div class="panel-footer p-b-none p-t-none">
                  <!-- Last Result -->
                  <div class="rpc-item-header ng-hide" ng-show="item.lastResult != null">
                    <a href="#" ng-click="showLastResult(item)">
                      <div class="header-icon m-r-md" style="margin-right: 8px;">
                        <i class="pe page-header-icon pe-7s-plus"></i>
                      </div>
                      <div class="header-title m-l-md"><h5 class="rpc-item-text">Last Result</h5>
                      </div>
                    </a>
                  </div>

                  <div class="rpc-item-result-miner_setGasPrice ng-hide"
                       ng-show="item.lastResult != null &amp;&amp; item.isLastResultVisible">
                    <pre class="panel panel-black-filled rpc-item-result ng-binding">null</pre>
                  </div>

                  <!-- Usage Sample -->
                  <div class="rpc-item-header flex-row flex-align-center rpc-usage">
                    <!--<a href="#" ng-click="showUsageHelp(item.methodName)">-->
                    <div class="header-icon m-l-none m-r-xs">
                      <i class="pe page-header-icon pe-7s-study"></i>
                    </div>
                    <pre class="panel panel-black-filled m-t-xs m-b-xs ng-binding">curl -X POST --data '{"jsonrpc":"2.0","method":"miner_setGasPrice","params":["0x0f4240"],"id":1}' <span
                      class="ng-binding">http://localhost:8080/rpc</span></pre>
                    <!--<div class="header-title"><h5 class="rpc-item-text">Curl</h5>-->
                    <!--</div>-->
                    <!--</a>-->

                  </div>
                </div>
              </div>
            </il><!-- end ngRepeat: item in rpcItems | rpcItemFilter:filterWord -->
            <il ng-repeat="item in rpcItems | rpcItemFilter:filterWord" class="ng-scope">
              <div class="panel panel-dark-filled">
                <div class="panel-heading p-b-none p-t-none">
                  <div class="row">
                    <div class="col-sm-6">
                      <u><h4 class="font-weight-normal ng-binding">miner_start</h4></u>
                    </div>
                    <div class="col-sm-3">
                      <h5 class="font-weight-normal ng-binding ng-hide" ng-show="item.count > 0">Invoked: 0</h5>
                    </div>
                    <div class="col-sm-3 m-l-none">
                      <h5 class="font-weight-normal ng-binding ng-hide" ng-show="item.lastTime">Last call: </h5>
                    </div>
                  </div>
                </div>

                <div class="panel-footer p-b-none p-t-none">
                  <!-- Last Result -->
                  <div class="rpc-item-header ng-hide" ng-show="item.lastResult != null">
                    <a href="#" ng-click="showLastResult(item)">
                      <div class="header-icon m-r-md" style="margin-right: 8px;">
                        <i class="pe page-header-icon pe-7s-plus"></i>
                      </div>
                      <div class="header-title m-l-md"><h5 class="rpc-item-text">Last Result</h5>
                      </div>
                    </a>
                  </div>

                  <div class="rpc-item-result-miner_start ng-hide"
                       ng-show="item.lastResult != null &amp;&amp; item.isLastResultVisible">
                    <pre class="panel panel-black-filled rpc-item-result ng-binding">null</pre>
                  </div>

                  <!-- Usage Sample -->
                  <div class="rpc-item-header flex-row flex-align-center rpc-usage">
                    <!--<a href="#" ng-click="showUsageHelp(item.methodName)">-->
                    <div class="header-icon m-l-none m-r-xs">
                      <i class="pe page-header-icon pe-7s-study"></i>
                    </div>
                    <pre class="panel panel-black-filled m-t-xs m-b-xs ng-binding">curl -X POST --data '{"jsonrpc":"2.0","method":"miner_start","params":[],"id":1}' <span
                      class="ng-binding">http://localhost:8080/rpc</span></pre>
                    <!--<div class="header-title"><h5 class="rpc-item-text">Curl</h5>-->
                    <!--</div>-->
                    <!--</a>-->

                  </div>
                </div>
              </div>
            </il><!-- end ngRepeat: item in rpcItems | rpcItemFilter:filterWord -->
            <il ng-repeat="item in rpcItems | rpcItemFilter:filterWord" class="ng-scope">
              <div class="panel panel-dark-filled">
                <div class="panel-heading p-b-none p-t-none">
                  <div class="row">
                    <div class="col-sm-6">
                      <u><h4 class="font-weight-normal ng-binding">miner_stop</h4></u>
                    </div>
                    <div class="col-sm-3">
                      <h5 class="font-weight-normal ng-binding ng-hide" ng-show="item.count > 0">Invoked: 0</h5>
                    </div>
                    <div class="col-sm-3 m-l-none">
                      <h5 class="font-weight-normal ng-binding ng-hide" ng-show="item.lastTime">Last call: </h5>
                    </div>
                  </div>
                </div>

                <div class="panel-footer p-b-none p-t-none">
                  <!-- Last Result -->
                  <div class="rpc-item-header ng-hide" ng-show="item.lastResult != null">
                    <a href="#" ng-click="showLastResult(item)">
                      <div class="header-icon m-r-md" style="margin-right: 8px;">
                        <i class="pe page-header-icon pe-7s-plus"></i>
                      </div>
                      <div class="header-title m-l-md"><h5 class="rpc-item-text">Last Result</h5>
                      </div>
                    </a>
                  </div>

                  <div class="rpc-item-result-miner_stop ng-hide"
                       ng-show="item.lastResult != null &amp;&amp; item.isLastResultVisible">
                    <pre class="panel panel-black-filled rpc-item-result ng-binding">null</pre>
                  </div>

                  <!-- Usage Sample -->
                  <div class="rpc-item-header flex-row flex-align-center rpc-usage">
                    <!--<a href="#" ng-click="showUsageHelp(item.methodName)">-->
                    <div class="header-icon m-l-none m-r-xs">
                      <i class="pe page-header-icon pe-7s-study"></i>
                    </div>
                    <pre class="panel panel-black-filled m-t-xs m-b-xs ng-binding">curl -X POST --data '{"jsonrpc":"2.0","method":"miner_stop","params":[],"id":1}' <span
                      class="ng-binding">http://localhost:8080/rpc</span></pre>
                    <!--<div class="header-title"><h5 class="rpc-item-text">Curl</h5>-->
                    <!--</div>-->
                    <!--</a>-->

                  </div>
                </div>
              </div>
            </il><!-- end ngRepeat: item in rpcItems | rpcItemFilter:filterWord -->
            <il ng-repeat="item in rpcItems | rpcItemFilter:filterWord" class="ng-scope">
              <div class="panel panel-dark-filled">
                <div class="panel-heading p-b-none p-t-none">
                  <div class="row">
                    <div class="col-sm-6">
                      <u><h4 class="font-weight-normal ng-binding">net_listening</h4></u>
                    </div>
                    <div class="col-sm-3">
                      <h5 class="font-weight-normal ng-binding ng-hide" ng-show="item.count > 0">Invoked: 0</h5>
                    </div>
                    <div class="col-sm-3 m-l-none">
                      <h5 class="font-weight-normal ng-binding ng-hide" ng-show="item.lastTime">Last call: </h5>
                    </div>
                  </div>
                </div>

                <div class="panel-footer p-b-none p-t-none">
                  <!-- Last Result -->
                  <div class="rpc-item-header ng-hide" ng-show="item.lastResult != null">
                    <a href="#" ng-click="showLastResult(item)">
                      <div class="header-icon m-r-md" style="margin-right: 8px;">
                        <i class="pe page-header-icon pe-7s-plus"></i>
                      </div>
                      <div class="header-title m-l-md"><h5 class="rpc-item-text">Last Result</h5>
                      </div>
                    </a>
                  </div>

                  <div class="rpc-item-result-net_listening ng-hide"
                       ng-show="item.lastResult != null &amp;&amp; item.isLastResultVisible">
                    <pre class="panel panel-black-filled rpc-item-result ng-binding">null</pre>
                  </div>

                  <!-- Usage Sample -->
                  <div class="rpc-item-header flex-row flex-align-center rpc-usage">
                    <!--<a href="#" ng-click="showUsageHelp(item.methodName)">-->
                    <div class="header-icon m-l-none m-r-xs">
                      <i class="pe page-header-icon pe-7s-study"></i>
                    </div>
                    <pre class="panel panel-black-filled m-t-xs m-b-xs ng-binding">curl -X POST --data '{"jsonrpc":"2.0","method":"net_listening","params":[],"id":67}' <span
                      class="ng-binding">http://localhost:8080/rpc</span></pre>
                    <!--<div class="header-title"><h5 class="rpc-item-text">Curl</h5>-->
                    <!--</div>-->
                    <!--</a>-->

                  </div>
                </div>
              </div>
            </il><!-- end ngRepeat: item in rpcItems | rpcItemFilter:filterWord -->
            <il ng-repeat="item in rpcItems | rpcItemFilter:filterWord" class="ng-scope">
              <div class="panel panel-dark-filled">
                <div class="panel-heading p-b-none p-t-none">
                  <div class="row">
                    <div class="col-sm-6">
                      <u><h4 class="font-weight-normal ng-binding">net_peerCount</h4></u>
                    </div>
                    <div class="col-sm-3">
                      <h5 class="font-weight-normal ng-binding ng-hide" ng-show="item.count > 0">Invoked: 0</h5>
                    </div>
                    <div class="col-sm-3 m-l-none">
                      <h5 class="font-weight-normal ng-binding ng-hide" ng-show="item.lastTime">Last call: </h5>
                    </div>
                  </div>
                </div>

                <div class="panel-footer p-b-none p-t-none">
                  <!-- Last Result -->
                  <div class="rpc-item-header ng-hide" ng-show="item.lastResult != null">
                    <a href="#" ng-click="showLastResult(item)">
                      <div class="header-icon m-r-md" style="margin-right: 8px;">
                        <i class="pe page-header-icon pe-7s-plus"></i>
                      </div>
                      <div class="header-title m-l-md"><h5 class="rpc-item-text">Last Result</h5>
                      </div>
                    </a>
                  </div>

                  <div class="rpc-item-result-net_peerCount ng-hide"
                       ng-show="item.lastResult != null &amp;&amp; item.isLastResultVisible">
                    <pre class="panel panel-black-filled rpc-item-result ng-binding">null</pre>
                  </div>

                  <!-- Usage Sample -->
                  <div class="rpc-item-header flex-row flex-align-center rpc-usage">
                    <!--<a href="#" ng-click="showUsageHelp(item.methodName)">-->
                    <div class="header-icon m-l-none m-r-xs">
                      <i class="pe page-header-icon pe-7s-study"></i>
                    </div>
                    <pre class="panel panel-black-filled m-t-xs m-b-xs ng-binding">curl -X POST --data '{"jsonrpc":"2.0","method":"net_peerCount","params":[],"id":74}' <span
                      class="ng-binding">http://localhost:8080/rpc</span></pre>
                    <!--<div class="header-title"><h5 class="rpc-item-text">Curl</h5>-->
                    <!--</div>-->
                    <!--</a>-->

                  </div>
                </div>
              </div>
            </il><!-- end ngRepeat: item in rpcItems | rpcItemFilter:filterWord -->
            <il ng-repeat="item in rpcItems | rpcItemFilter:filterWord" class="ng-scope">
              <div class="panel panel-dark-filled">
                <div class="panel-heading p-b-none p-t-none">
                  <div class="row">
                    <div class="col-sm-6">
                      <u><h4 class="font-weight-normal ng-binding">net_version</h4></u>
                    </div>
                    <div class="col-sm-3">
                      <h5 class="font-weight-normal ng-binding ng-hide" ng-show="item.count > 0">Invoked: 0</h5>
                    </div>
                    <div class="col-sm-3 m-l-none">
                      <h5 class="font-weight-normal ng-binding ng-hide" ng-show="item.lastTime">Last call: </h5>
                    </div>
                  </div>
                </div>

                <div class="panel-footer p-b-none p-t-none">
                  <!-- Last Result -->
                  <div class="rpc-item-header ng-hide" ng-show="item.lastResult != null">
                    <a href="#" ng-click="showLastResult(item)">
                      <div class="header-icon m-r-md" style="margin-right: 8px;">
                        <i class="pe page-header-icon pe-7s-plus"></i>
                      </div>
                      <div class="header-title m-l-md"><h5 class="rpc-item-text">Last Result</h5>
                      </div>
                    </a>
                  </div>

                  <div class="rpc-item-result-net_version ng-hide"
                       ng-show="item.lastResult != null &amp;&amp; item.isLastResultVisible">
                    <pre class="panel panel-black-filled rpc-item-result ng-binding">null</pre>
                  </div>

                  <!-- Usage Sample -->
                  <div class="rpc-item-header flex-row flex-align-center rpc-usage">
                    <!--<a href="#" ng-click="showUsageHelp(item.methodName)">-->
                    <div class="header-icon m-l-none m-r-xs">
                      <i class="pe page-header-icon pe-7s-study"></i>
                    </div>
                    <pre class="panel panel-black-filled m-t-xs m-b-xs ng-binding">curl -X POST --data '{"jsonrpc":"2.0","method":"net_version","params":[],"id":67}' <span
                      class="ng-binding">http://localhost:8080/rpc</span></pre>
                    <!--<div class="header-title"><h5 class="rpc-item-text">Curl</h5>-->
                    <!--</div>-->
                    <!--</a>-->

                  </div>
                </div>
              </div>
            </il><!-- end ngRepeat: item in rpcItems | rpcItemFilter:filterWord -->
            <il ng-repeat="item in rpcItems | rpcItemFilter:filterWord" class="ng-scope">
              <div class="panel panel-dark-filled">
                <div class="panel-heading p-b-none p-t-none">
                  <div class="row">
                    <div class="col-sm-6">
                      <u><h4 class="font-weight-normal ng-binding">personal_importRawKey</h4></u>
                    </div>
                    <div class="col-sm-3">
                      <h5 class="font-weight-normal ng-binding ng-hide" ng-show="item.count > 0">Invoked: 0</h5>
                    </div>
                    <div class="col-sm-3 m-l-none">
                      <h5 class="font-weight-normal ng-binding ng-hide" ng-show="item.lastTime">Last call: </h5>
                    </div>
                  </div>
                </div>

                <div class="panel-footer p-b-none p-t-none">
                  <!-- Last Result -->
                  <div class="rpc-item-header ng-hide" ng-show="item.lastResult != null">
                    <a href="#" ng-click="showLastResult(item)">
                      <div class="header-icon m-r-md" style="margin-right: 8px;">
                        <i class="pe page-header-icon pe-7s-plus"></i>
                      </div>
                      <div class="header-title m-l-md"><h5 class="rpc-item-text">Last Result</h5>
                      </div>
                    </a>
                  </div>

                  <div class="rpc-item-result-personal_importRawKey ng-hide"
                       ng-show="item.lastResult != null &amp;&amp; item.isLastResultVisible">
                    <pre class="panel panel-black-filled rpc-item-result ng-binding">null</pre>
                  </div>

                  <!-- Usage Sample -->
                  <div class="rpc-item-header flex-row flex-align-center rpc-usage">
                    <!--<a href="#" ng-click="showUsageHelp(item.methodName)">-->
                    <div class="header-icon m-l-none m-r-xs">
                      <i class="pe page-header-icon pe-7s-study"></i>
                    </div>
                    <pre class="panel panel-black-filled m-t-xs m-b-xs ng-binding">curl -X POST --data '{"jsonrpc":"2.0","method":"personal_importRawKey","params":["privateKey", "password"],"id":1}' <span
                      class="ng-binding">http://localhost:8080/rpc</span></pre>
                    <!--<div class="header-title"><h5 class="rpc-item-text">Curl</h5>-->
                    <!--</div>-->
                    <!--</a>-->

                  </div>
                </div>
              </div>
            </il><!-- end ngRepeat: item in rpcItems | rpcItemFilter:filterWord -->
            <il ng-repeat="item in rpcItems | rpcItemFilter:filterWord" class="ng-scope">
              <div class="panel panel-dark-filled">
                <div class="panel-heading p-b-none p-t-none">
                  <div class="row">
                    <div class="col-sm-6">
                      <u><h4 class="font-weight-normal ng-binding">personal_listAccounts</h4></u>
                    </div>
                    <div class="col-sm-3">
                      <h5 class="font-weight-normal ng-binding ng-hide" ng-show="item.count > 0">Invoked: 0</h5>
                    </div>
                    <div class="col-sm-3 m-l-none">
                      <h5 class="font-weight-normal ng-binding ng-hide" ng-show="item.lastTime">Last call: </h5>
                    </div>
                  </div>
                </div>

                <div class="panel-footer p-b-none p-t-none">
                  <!-- Last Result -->
                  <div class="rpc-item-header ng-hide" ng-show="item.lastResult != null">
                    <a href="#" ng-click="showLastResult(item)">
                      <div class="header-icon m-r-md" style="margin-right: 8px;">
                        <i class="pe page-header-icon pe-7s-plus"></i>
                      </div>
                      <div class="header-title m-l-md"><h5 class="rpc-item-text">Last Result</h5>
                      </div>
                    </a>
                  </div>

                  <div class="rpc-item-result-personal_listAccounts ng-hide"
                       ng-show="item.lastResult != null &amp;&amp; item.isLastResultVisible">
                    <pre class="panel panel-black-filled rpc-item-result ng-binding">null</pre>
                  </div>

                  <!-- Usage Sample -->
                  <div class="rpc-item-header flex-row flex-align-center rpc-usage">
                    <!--<a href="#" ng-click="showUsageHelp(item.methodName)">-->
                    <div class="header-icon m-l-none m-r-xs">
                      <i class="pe page-header-icon pe-7s-study"></i>
                    </div>
                    <pre class="panel panel-black-filled m-t-xs m-b-xs ng-binding">curl -X POST --data '{"jsonrpc":"2.0","method":"personal_listAccounts","params":[],"id":64}' <span
                      class="ng-binding">http://localhost:8080/rpc</span></pre>
                    <!--<div class="header-title"><h5 class="rpc-item-text">Curl</h5>-->
                    <!--</div>-->
                    <!--</a>-->

                  </div>
                </div>
              </div>
            </il><!-- end ngRepeat: item in rpcItems | rpcItemFilter:filterWord -->
            <il ng-repeat="item in rpcItems | rpcItemFilter:filterWord" class="ng-scope">
              <div class="panel panel-dark-filled">
                <div class="panel-heading p-b-none p-t-none">
                  <div class="row">
                    <div class="col-sm-6">
                      <u><h4 class="font-weight-normal ng-binding">personal_lockAccount</h4></u>
                    </div>
                    <div class="col-sm-3">
                      <h5 class="font-weight-normal ng-binding ng-hide" ng-show="item.count > 0">Invoked: 0</h5>
                    </div>
                    <div class="col-sm-3 m-l-none">
                      <h5 class="font-weight-normal ng-binding ng-hide" ng-show="item.lastTime">Last call: </h5>
                    </div>
                  </div>
                </div>

                <div class="panel-footer p-b-none p-t-none">
                  <!-- Last Result -->
                  <div class="rpc-item-header ng-hide" ng-show="item.lastResult != null">
                    <a href="#" ng-click="showLastResult(item)">
                      <div class="header-icon m-r-md" style="margin-right: 8px;">
                        <i class="pe page-header-icon pe-7s-plus"></i>
                      </div>
                      <div class="header-title m-l-md"><h5 class="rpc-item-text">Last Result</h5>
                      </div>
                    </a>
                  </div>

                  <div class="rpc-item-result-personal_lockAccount ng-hide"
                       ng-show="item.lastResult != null &amp;&amp; item.isLastResultVisible">
                    <pre class="panel panel-black-filled rpc-item-result ng-binding">null</pre>
                  </div>

                  <!-- Usage Sample -->
                  <div class="rpc-item-header flex-row flex-align-center rpc-usage">
                    <!--<a href="#" ng-click="showUsageHelp(item.methodName)">-->
                    <div class="header-icon m-l-none m-r-xs">
                      <i class="pe page-header-icon pe-7s-study"></i>
                    </div>
                    <pre class="panel panel-black-filled m-t-xs m-b-xs ng-binding">curl -X POST --data '{"jsonrpc":"2.0","method":"personal_lockAccount","params":["0xcd2a3d9f938e13cd947ec05abc7fe734df8dd826"],"id":1}' <span
                      class="ng-binding">http://localhost:8080/rpc</span></pre>
                    <!--<div class="header-title"><h5 class="rpc-item-text">Curl</h5>-->
                    <!--</div>-->
                    <!--</a>-->

                  </div>
                </div>
              </div>
            </il><!-- end ngRepeat: item in rpcItems | rpcItemFilter:filterWord -->
            <il ng-repeat="item in rpcItems | rpcItemFilter:filterWord" class="ng-scope">
              <div class="panel panel-dark-filled">
                <div class="panel-heading p-b-none p-t-none">
                  <div class="row">
                    <div class="col-sm-6">
                      <u><h4 class="font-weight-normal ng-binding">personal_newAccount</h4></u>
                    </div>
                    <div class="col-sm-3">
                      <h5 class="font-weight-normal ng-binding ng-hide" ng-show="item.count > 0">Invoked: 0</h5>
                    </div>
                    <div class="col-sm-3 m-l-none">
                      <h5 class="font-weight-normal ng-binding ng-hide" ng-show="item.lastTime">Last call: </h5>
                    </div>
                  </div>
                </div>

                <div class="panel-footer p-b-none p-t-none">
                  <!-- Last Result -->
                  <div class="rpc-item-header ng-hide" ng-show="item.lastResult != null">
                    <a href="#" ng-click="showLastResult(item)">
                      <div class="header-icon m-r-md" style="margin-right: 8px;">
                        <i class="pe page-header-icon pe-7s-plus"></i>
                      </div>
                      <div class="header-title m-l-md"><h5 class="rpc-item-text">Last Result</h5>
                      </div>
                    </a>
                  </div>

                  <div class="rpc-item-result-personal_newAccount ng-hide"
                       ng-show="item.lastResult != null &amp;&amp; item.isLastResultVisible">
                    <pre class="panel panel-black-filled rpc-item-result ng-binding">null</pre>
                  </div>

                  <!-- Usage Sample -->
                  <div class="rpc-item-header flex-row flex-align-center rpc-usage">
                    <!--<a href="#" ng-click="showUsageHelp(item.methodName)">-->
                    <div class="header-icon m-l-none m-r-xs">
                      <i class="pe page-header-icon pe-7s-study"></i>
                    </div>
                    <pre class="panel panel-black-filled m-t-xs m-b-xs ng-binding">curl -X POST --data '{"jsonrpc":"2.0","method":"personal_newAccount","params":["passphrase"],"id":1}' <span
                      class="ng-binding">http://localhost:8080/rpc</span></pre>
                    <!--<div class="header-title"><h5 class="rpc-item-text">Curl</h5>-->
                    <!--</div>-->
                    <!--</a>-->

                  </div>
                </div>
              </div>
            </il><!-- end ngRepeat: item in rpcItems | rpcItemFilter:filterWord -->
            <il ng-repeat="item in rpcItems | rpcItemFilter:filterWord" class="ng-scope">
              <div class="panel panel-dark-filled">
                <div class="panel-heading p-b-none p-t-none">
                  <div class="row">
                    <div class="col-sm-6">
                      <u><h4 class="font-weight-normal ng-binding">personal_signAndSendTransaction</h4></u>
                    </div>
                    <div class="col-sm-3">
                      <h5 class="font-weight-normal ng-binding ng-hide" ng-show="item.count > 0">Invoked: 0</h5>
                    </div>
                    <div class="col-sm-3 m-l-none">
                      <h5 class="font-weight-normal ng-binding ng-hide" ng-show="item.lastTime">Last call: </h5>
                    </div>
                  </div>
                </div>

                <div class="panel-footer p-b-none p-t-none">
                  <!-- Last Result -->
                  <div class="rpc-item-header ng-hide" ng-show="item.lastResult != null">
                    <a href="#" ng-click="showLastResult(item)">
                      <div class="header-icon m-r-md" style="margin-right: 8px;">
                        <i class="pe page-header-icon pe-7s-plus"></i>
                      </div>
                      <div class="header-title m-l-md"><h5 class="rpc-item-text">Last Result</h5>
                      </div>
                    </a>
                  </div>

                  <div class="rpc-item-result-personal_signAndSendTransaction ng-hide"
                       ng-show="item.lastResult != null &amp;&amp; item.isLastResultVisible">
                    <pre class="panel panel-black-filled rpc-item-result ng-binding">null</pre>
                  </div>

                  <!-- Usage Sample -->
                  <div class="rpc-item-header flex-row flex-align-center rpc-usage">
                    <!--<a href="#" ng-click="showUsageHelp(item.methodName)">-->
                    <div class="header-icon m-l-none m-r-xs">
                      <i class="pe page-header-icon pe-7s-study"></i>
                    </div>
                    <pre class="panel panel-black-filled m-t-xs m-b-xs ng-binding">curl -X POST --data '{"jsonrpc":"2.0","method":"personal_signAndSendTransaction","params":["0x0", "0x0"],"id":64}' <span
                      class="ng-binding">http://localhost:8080/rpc</span></pre>
                    <!--<div class="header-title"><h5 class="rpc-item-text">Curl</h5>-->
                    <!--</div>-->
                    <!--</a>-->

                  </div>
                </div>
              </div>
            </il><!-- end ngRepeat: item in rpcItems | rpcItemFilter:filterWord -->
            <il ng-repeat="item in rpcItems | rpcItemFilter:filterWord" class="ng-scope">
              <div class="panel panel-dark-filled">
                <div class="panel-heading p-b-none p-t-none">
                  <div class="row">
                    <div class="col-sm-6">
                      <u><h4 class="font-weight-normal ng-binding">personal_unlockAccount</h4></u>
                    </div>
                    <div class="col-sm-3">
                      <h5 class="font-weight-normal ng-binding ng-hide" ng-show="item.count > 0">Invoked: 0</h5>
                    </div>
                    <div class="col-sm-3 m-l-none">
                      <h5 class="font-weight-normal ng-binding ng-hide" ng-show="item.lastTime">Last call: </h5>
                    </div>
                  </div>
                </div>

                <div class="panel-footer p-b-none p-t-none">
                  <!-- Last Result -->
                  <div class="rpc-item-header ng-hide" ng-show="item.lastResult != null">
                    <a href="#" ng-click="showLastResult(item)">
                      <div class="header-icon m-r-md" style="margin-right: 8px;">
                        <i class="pe page-header-icon pe-7s-plus"></i>
                      </div>
                      <div class="header-title m-l-md"><h5 class="rpc-item-text">Last Result</h5>
                      </div>
                    </a>
                  </div>

                  <div class="rpc-item-result-personal_unlockAccount ng-hide"
                       ng-show="item.lastResult != null &amp;&amp; item.isLastResultVisible">
                    <pre class="panel panel-black-filled rpc-item-result ng-binding">null</pre>
                  </div>

                  <!-- Usage Sample -->
                  <div class="rpc-item-header flex-row flex-align-center rpc-usage">
                    <!--<a href="#" ng-click="showUsageHelp(item.methodName)">-->
                    <div class="header-icon m-l-none m-r-xs">
                      <i class="pe page-header-icon pe-7s-study"></i>
                    </div>
                    <pre class="panel panel-black-filled m-t-xs m-b-xs ng-binding">curl -X POST --data '{"jsonrpc":"2.0","method":"personal_unlockAccount","params":["0xcd2a3d9f938e13cd947ec05abc7fe734df8dd826", "passphrase"],"id":1}' <span
                      class="ng-binding">http://localhost:8080/rpc</span></pre>
                    <!--<div class="header-title"><h5 class="rpc-item-text">Curl</h5>-->
                    <!--</div>-->
                    <!--</a>-->

                  </div>
                </div>
              </div>
            </il><!-- end ngRepeat: item in rpcItems | rpcItemFilter:filterWord -->
            <il ng-repeat="item in rpcItems | rpcItemFilter:filterWord" class="ng-scope">
              <div class="panel panel-dark-filled">
                <div class="panel-heading p-b-none p-t-none">
                  <div class="row">
                    <div class="col-sm-6">
                      <u><h4 class="font-weight-normal ng-binding">shh_version</h4></u>
                    </div>
                    <div class="col-sm-3">
                      <h5 class="font-weight-normal ng-binding ng-hide" ng-show="item.count > 0">Invoked: 0</h5>
                    </div>
                    <div class="col-sm-3 m-l-none">
                      <h5 class="font-weight-normal ng-binding ng-hide" ng-show="item.lastTime">Last call: </h5>
                    </div>
                  </div>
                </div>

                <div class="panel-footer p-b-none p-t-none">
                  <!-- Last Result -->
                  <div class="rpc-item-header ng-hide" ng-show="item.lastResult != null">
                    <a href="#" ng-click="showLastResult(item)">
                      <div class="header-icon m-r-md" style="margin-right: 8px;">
                        <i class="pe page-header-icon pe-7s-plus"></i>
                      </div>
                      <div class="header-title m-l-md"><h5 class="rpc-item-text">Last Result</h5>
                      </div>
                    </a>
                  </div>

                  <div class="rpc-item-result-shh_version ng-hide"
                       ng-show="item.lastResult != null &amp;&amp; item.isLastResultVisible">
                    <pre class="panel panel-black-filled rpc-item-result ng-binding">null</pre>
                  </div>

                  <!-- Usage Sample -->
                  <div class="rpc-item-header flex-row flex-align-center rpc-usage">
                    <!--<a href="#" ng-click="showUsageHelp(item.methodName)">-->
                    <div class="header-icon m-l-none m-r-xs">
                      <i class="pe page-header-icon pe-7s-study"></i>
                    </div>
                    <pre class="panel panel-black-filled m-t-xs m-b-xs ng-binding">curl -X POST --data '{"jsonrpc":"2.0","method":"shh_version","params":[],"id":67}' <span
                      class="ng-binding">http://localhost:8080/rpc</span></pre>
                    <!--<div class="header-title"><h5 class="rpc-item-text">Curl</h5>-->
                    <!--</div>-->
                    <!--</a>-->

                  </div>
                </div>
              </div>
            </il><!-- end ngRepeat: item in rpcItems | rpcItemFilter:filterWord -->
            <il ng-repeat="item in rpcItems | rpcItemFilter:filterWord" class="ng-scope">
              <div class="panel panel-dark-filled">
                <div class="panel-heading p-b-none p-t-none">
                  <div class="row">
                    <div class="col-sm-6">
                      <u><h4 class="font-weight-normal ng-binding">web3_clientVersion</h4></u>
                    </div>
                    <div class="col-sm-3">
                      <h5 class="font-weight-normal ng-binding ng-hide" ng-show="item.count > 0">Invoked: 0</h5>
                    </div>
                    <div class="col-sm-3 m-l-none">
                      <h5 class="font-weight-normal ng-binding ng-hide" ng-show="item.lastTime">Last call: </h5>
                    </div>
                  </div>
                </div>

                <div class="panel-footer p-b-none p-t-none">
                  <!-- Last Result -->
                  <div class="rpc-item-header ng-hide" ng-show="item.lastResult != null">
                    <a href="#" ng-click="showLastResult(item)">
                      <div class="header-icon m-r-md" style="margin-right: 8px;">
                        <i class="pe page-header-icon pe-7s-plus"></i>
                      </div>
                      <div class="header-title m-l-md"><h5 class="rpc-item-text">Last Result</h5>
                      </div>
                    </a>
                  </div>

                  <div class="rpc-item-result-web3_clientVersion ng-hide"
                       ng-show="item.lastResult != null &amp;&amp; item.isLastResultVisible">
                    <pre class="panel panel-black-filled rpc-item-result ng-binding">null</pre>
                  </div>

                  <!-- Usage Sample -->
                  <div class="rpc-item-header flex-row flex-align-center rpc-usage">
                    <!--<a href="#" ng-click="showUsageHelp(item.methodName)">-->
                    <div class="header-icon m-l-none m-r-xs">
                      <i class="pe page-header-icon pe-7s-study"></i>
                    </div>
                    <pre class="panel panel-black-filled m-t-xs m-b-xs ng-binding">curl -X POST --data '{"jsonrpc":"2.0","method":"web3_clientVersion","params":[],"id":67}' <span
                      class="ng-binding">http://localhost:8080/rpc</span></pre>
                    <!--<div class="header-title"><h5 class="rpc-item-text">Curl</h5>-->
                    <!--</div>-->
                    <!--</a>-->

                  </div>
                </div>
              </div>
            </il><!-- end ngRepeat: item in rpcItems | rpcItemFilter:filterWord -->
            <il ng-repeat="item in rpcItems | rpcItemFilter:filterWord" class="ng-scope">
              <div class="panel panel-dark-filled">
                <div class="panel-heading p-b-none p-t-none">
                  <div class="row">
                    <div class="col-sm-6">
                      <u><h4 class="font-weight-normal ng-binding">web3_sha3</h4></u>
                    </div>
                    <div class="col-sm-3">
                      <h5 class="font-weight-normal ng-binding ng-hide" ng-show="item.count > 0">Invoked: 0</h5>
                    </div>
                    <div class="col-sm-3 m-l-none">
                      <h5 class="font-weight-normal ng-binding ng-hide" ng-show="item.lastTime">Last call: </h5>
                    </div>
                  </div>
                </div>

                <div class="panel-footer p-b-none p-t-none">
                  <!-- Last Result -->
                  <div class="rpc-item-header ng-hide" ng-show="item.lastResult != null">
                    <a href="#" ng-click="showLastResult(item)">
                      <div class="header-icon m-r-md" style="margin-right: 8px;">
                        <i class="pe page-header-icon pe-7s-plus"></i>
                      </div>
                      <div class="header-title m-l-md"><h5 class="rpc-item-text">Last Result</h5>
                      </div>
                    </a>
                  </div>

                  <div class="rpc-item-result-web3_sha3 ng-hide"
                       ng-show="item.lastResult != null &amp;&amp; item.isLastResultVisible">
                    <pre class="panel panel-black-filled rpc-item-result ng-binding">null</pre>
                  </div>

                  <!-- Usage Sample -->
                  <div class="rpc-item-header flex-row flex-align-center rpc-usage">
                    <!--<a href="#" ng-click="showUsageHelp(item.methodName)">-->
                    <div class="header-icon m-l-none m-r-xs">
                      <i class="pe page-header-icon pe-7s-study"></i>
                    </div>
                    <pre class="panel panel-black-filled m-t-xs m-b-xs ng-binding">curl -X POST --data '{"jsonrpc":"2.0","method":"web3_sha3","params":["0x68656c6c6f20776f726c64"],"id":64}' <span
                      class="ng-binding">http://localhost:8080/rpc</span></pre>
                    <!--<div class="header-title"><h5 class="rpc-item-text">Curl</h5>-->
                    <!--</div>-->
                    <!--</a>-->

                  </div>
                </div>
              </div>
            </il><!-- end ngRepeat: item in rpcItems | rpcItemFilter:filterWord -->
          </ul>
        </div>
        <div id="mCSB_3_scrollbar_vertical" class="mCSB_scrollTools mCSB_3_scrollbar mCS-dark mCSB_scrollTools_vertical"
             style="display: block;">
          <div class="mCSB_draggerContainer">
            <div id="mCSB_3_dragger_vertical" class="mCSB_dragger"
                 style="position: absolute; min-height: 30px; height: 51px; top: 0px; display: block; max-height: 665px;">
              <div class="mCSB_dragger_bar" style="line-height: 30px;">
              </div>
            </div>
            <div class="mCSB_draggerRail">
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    name: "RpcUsage"
  }
</script>

<style scoped>

</style>
