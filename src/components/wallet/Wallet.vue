<template>
  <div class="container-fluid">
    <div class="row">
      <div class="col-lg-12">
        <div class="view-header">

          <div class="pull-right text-right text-14">
            <h3 class="ng-binding">10 ETHER</h3>
            <p class="ng-binding">$n/a</p>
          </div>

          <div class="header-icon">
            <i class="pe page-header-icon pe-7s-wallet"></i>
          </div>
          <div class="header-title">
            <h3 class="m-b-xs">Wallet</h3>
            <small>
              Allows to receive and send ETH
            </small>
          </div>
        </div>
        <hr>
      </div>
    </div>

    <div class="row">
      <div class="col-lg-12">
        <div class="panel panel-filled">
          <div class="panel-heading">
            My Wallet Addresses
          </div>
          <div class="panel-heading">
            <a href="#" ng-click="onNewAddress()" class="btn btn-w-md btn-primary"><span class="pe-7s-key m-r-sm"></span>New address in keystore</a>
            <span class="m-l-sm"></span>
            <a href="#" ng-click="onPhraseAddress()" class="btn btn-w-md btn-primary">New mnemonic address</a>
            <span class="m-l-sm"></span>
            <a href="#" ng-click="onImportAddress()" class="btn btn-w-md btn-primary"><i class="fa fa-eye m-r-sm"></i>Import address</a>
          </div>

          <div class="table-responsive mCustomScrollbar _mCS_7 mCS-autoHide mCS_no_scrollbar" id="address-scroll-container" style="height: 568px;"><div id="mCSB_7" class="mCustomScrollBox mCS-dark mCSB_vertical mCSB_inside" tabindex="0" style="max-height: none;"><div id="mCSB_7_container" class="mCSB_container mCS_y_hidden mCS_no_scrollbar_y" style="position:relative; top:0; left:0;" dir="ltr">
            <table class="table">
              <thead>
              </thead>
              <tbody>
              <!-- ngRepeat: item in addresses --><tr ng-repeat="item in addresses" class="ng-scope">
                <td>
                  <span class="pe-7s-key m-l-sm" ng-hide="!item.hasKeystoreKey"></span>
                </td>
                <td class="ng-binding">
                  Account 1
                </td>
                <td>
                  <div class="font-monospace ng-binding">0xb240ceA42BA70aaC76de6A0E7aa171DF9C9a7166</div>
                </td>
                <td>
                  <span class="c-white ng-binding">10</span> <span data-toggle="tooltip" title="Pending amount" class="ng-binding"></span>
                </td>
                <td>
                  <a href="#" ng-click="onSendClick(item)">Send Amount</a>
                </td>
                <td>
                  <a href="#" ng-click="onRemoveClick(item)">Remove Address</a>
                </td>
              </tr><!-- end ngRepeat: item in addresses -->
              </tbody>
            </table>
          </div><div id="mCSB_7_scrollbar_vertical" class="mCSB_scrollTools mCSB_7_scrollbar mCS-dark mCSB_scrollTools_vertical" style="display: none;"><div class="mCSB_draggerContainer"><div id="mCSB_7_dragger_vertical" class="mCSB_dragger" style="position: absolute; min-height: 30px; height: 0px; top: 0px;"><div class="mCSB_dragger_bar" style="line-height: 30px;"></div></div><div class="mCSB_draggerRail"></div></div></div></div></div>
        </div>

        <div class="panel panel-filled">
          <div class="panel-heading">
            Last Transactions
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
    export default {
        name: "Wallet"
    }
</script>

<style scoped>

</style>
