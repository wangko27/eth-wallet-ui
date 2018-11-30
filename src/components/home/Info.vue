<template>
  <div class="panel panel-filled">
    <form class="form-horizontal home-info-text panel-body ng-pristine ng-valid">
      <div class="home-info-row">
        <div class="col-sm-4">
          Network:
        </div>
        <div class="col-sm-6 ng-binding">
          Private Miner Network
        </div>
      </div>

      <div class="home-info-row">
        <div class="col-sm-4">
          Genesis:
        </div>
        <!-- ngIf: vm.data.featureRpc --><div class="col-sm-6 ng-scope" ng-if="vm.data.featureRpc">
        <a href="/terminal#eth_getBlockByNumber%200%20true" class="ng-binding">0xc4722e</a>
      </div><!-- end ngIf: vm.data.featureRpc -->
        <!-- ngIf: !vm.data.featureRpc -->
      </div>

      <div class="home-info-row">
        <div class="col-sm-4">
          Sync status:
        </div>
        <div class="col-sm-8 ng-binding">
          Short sync
        </div>
      </div>

      <div class="home-info-row">
        <div class="col-sm-4">
          Mine status:
        </div>
        <div class="col-sm-6 ng-binding">
          Mining
        </div>
      </div>

      <div class="home-info-row">
        <div class="col-sm-4">
          Active peers:
        </div>
        <div class="col-sm-6 ng-binding">
          0
        </div>
      </div>

      <div class="home-info-row">
        <div class="col-sm-4">
          NodeID:
        </div>
        <!-- ngIf: vm.data.featureRpc --><div class="col-sm-6 ng-scope" ng-if="vm.data.featureRpc">
        <a href="/terminal#admin_nodeInfo" class="ng-binding">0x024631</a>
      </div><!-- end ngIf: vm.data.featureRpc -->
        <!-- ngIf: !vm.data.featureRpc -->
      </div>

      <div class="home-info-row">
        <div class="col-sm-4 ng-binding">
          IP:
        </div>
        <div class="col-sm-4 ng-binding">
          0.0.0.0
        </div>
        <div class="col-sm-4">
          <a id="testPortsLink" href="#">Test ports</a>
        </div>
      </div>

      <div class="home-info-row">
        <div class="col-sm-4">
          Eth port:
        </div>
        <div class="col-sm-8 ng-binding">
          30303   <span class="font-sans-serif" data-toggle="tooltip" title="Test result if your TCP port 30303 is accessible for incoming connections from internet">[<span class="port-test-result">?</span>]</span>
        </div>
      </div>

      <div class="home-info-row">
        <div class="col-sm-4">
          JsonRPC port:
        </div>
        <div class="col-sm-8 ng-binding">
          8545   <span class="font-sans-serif" data-toggle="tooltip" title="Test result if your TCP port 8545 is accessible for incoming connections from internet">[<span class="port-test-result">?</span>]</span>
        </div>
      </div>

    </form>
  </div>
</template>

<script>
    export default {
        name: "Info"
    }
</script>

<style scoped>

</style>
