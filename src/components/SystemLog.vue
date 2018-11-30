<template>
  <div class="container-fluid">
    <div class="row">
      <div class="col-lg-12">
        <div class="view-header">

          <div class="m-l-sm pull-right text-right text-14">
            <form class="navbar-form navbar-right ng-pristine ng-valid" role="search">
              <ul class="list-inline">
                <li>
                  <div class="checkbox">
                    <label>
                      <input type="checkbox" ng-model="isAutoScroll" ng-change="onAutoScrollChange()"
                             class="ng-pristine ng-untouched ng-valid ng-not-empty">
                      Auto-scroll
                    </label>
                  </div>
                </li>

                <li>
                  <div class="form-group">
                    <input type="text" class="form-control query" placeholder="Filter" tabindex="1">
                  </div>
                </li>

              </ul>
            </form>
          </div>

          <div class="header-icon">
            <i class="pe page-header-icon pe-7s-news-paper"></i>
          </div>

          <div class="header-title">
            <h3 class="m-b-xs">System Logs</h3>
            <small>
              Displaying active peers and their countries on the map.
            </small>
          </div>
        </div>
        <hr>
      </div>
    </div>

    <div class="panel panel-filled">
      <div id="log-scroll-container" class="bs-example mCustomScrollbar _mCS_1 mCS-autoHide" style="height: 674px;">
        <div id="mCSB_1" class="mCustomScrollBox mCS-dark mCSB_vertical mCSB_inside" style="max-height: none;"
             tabindex="0">
          <div id="mCSB_1_container" class="mCSB_container" style="position: relative; top: -83115px; left: 0px;"
               dir="ltr">
            <pre class="log"><div class="line"><p class="inner-line">2018-11-30 07:25:13,619 INFO  [WireTrafficStats-0] net - UDP: Speed in/out 0b / 0b(sec), packets in/out 0/0, total in/out: 0b / 0b
</p></div><div class="line"><p class="inner-line">2018-11-30 07:25:13,674 INFO  [pool-5-thread-1] sync - Sync state: Complete, last block #7338, best known #7338
</p></div><div class="line"><p class="inner-line">2018-11-30 07:25:20,597 INFO  [ethash-pool-2] harmony - blockMined
</p></div><div class="line"><p class="inner-line">2018-11-30 07:25:20,598 INFO  [ethash-pool-2] mine - Wow, block mined !!!: f90213f9020ea068cde3e91d2ad3729cc7ed65c014771b45ac7f40341011cdde51e1dd54a2259fa01dcc4de8dec75d7aab85b567b6ccd41ad312451b948a7413f0a142fd40d4934794cd2a3d9f938e13cd947ec05abc7fe734df8dd826a05c9a1de6c8922e0eb617d5a98bb131ce1d8e8b6167887eabafb9c3d8349366fea056e81f171bcc55a6ff8345e692c0f86e5b48e01b996cadc001622fb5e363b421a056e81f171bcc55a6ff8345e692c0f86e5b48e01b996cadc001622fb5e363b421b9010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000830499aa821cab871388000000000080845c00e5d091457468657265756d4a20706f7765726564a09216a64be115c070ed969927cc6ca53a200564eb2430e0b2bed99672fcd3903688977769e15d3bce92c0c0
BlockData [   hash=1bd163b0778bbbe8cff70ac8f822ea3f4e5f19305c2ce8eb8afbef98a94ff394
  parentHash=68cde3e91d2ad3729cc7ed65c014771b45ac7f40341011cdde51e1dd54a2259f
  unclesHash=1dcc4de8dec75d7aab85b567b6ccd41ad312451b948a7413f0a142fd40d49347
  coinbase=cd2a3d9f938e13cd947ec05abc7fe734df8dd826
  stateRoot=5c9a1de6c8922e0eb617d5a98bb131ce1d8e8b6167887eabafb9c3d8349366fe
  txTrieHash=56e81f171bcc55a6ff8345e692c0f86e5b48e01b996cadc001622fb5e363b421
  receiptsTrieHash=56e81f171bcc55a6ff8345e692c0f86e5b48e01b996cadc001622fb5e363b421
  difficulty=0499aa
  number=7339
  gasLimit=13880000000000
  gasUsed=0
  timestamp=1543562704 (2018.11.30 07:25:04)
  extraData=457468657265756d4a20706f7765726564
  mixHash=9216a64be115c070ed969927cc6ca53a200564eb2430e0b2bed99672fcd39036
  nonce=977769e15d3bce92
Uncles []
Txs []
</p></div><div class="line"><p class="inner-line">2018-11-30 07:46:26,589 INFO  [DbFlushManagerThread-0] db - Flush started
</p></div><div class="line"><p class="inner-line">2018-11-30 07:46:26,590 INFO  [DbFlushManagerThread-0] db - Flush completed in 1 ms
</p></div><div class="line"><p class="inner-line">2018-11-30 07:46:26,591 INFO  [EDT] harmony - new block mining started
</p></div></pre>
          </div>
          <div id="mCSB_1_scrollbar_vertical"
               class="mCSB_scrollTools mCSB_1_scrollbar mCS-dark mCSB_scrollTools_vertical" style="display: block;">
            <div class="mCSB_draggerContainer">
              <div id="mCSB_1_dragger_vertical" class="mCSB_dragger"
                   style="position: absolute; min-height: 30px; height: 5px; top: 624px; display: block; max-height: 644px;">
                <div class="mCSB_dragger_bar" style="line-height: 30px;"></div>
              </div>
              <div class="mCSB_draggerRail"></div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    name: "SystemLog"
  }
</script>

<style scoped>

</style>
