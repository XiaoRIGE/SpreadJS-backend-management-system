<template>
  <div id="spread-host">
    <gc-spread-sheets hostClass="spreadHost" @workbookInitialized="initWorkbook">
    </gc-spread-sheets>
  </div>
</template>

<script setup>
import "@grapecity/spread-sheets/styles/gc.spread.sheets.excel2016colorful.css";
import * as GC from "@grapecity/spread-sheets";
function initWorkbook(spread) {
  let sheet = spread.getActiveSheet();
  sheet
    .getCell(0, 0)
    .vAlign(GC.Spread.Sheets.VerticalAlign.center)
    .value("Hello SpreadJS");
}
</script>

<style>
.spreadHost {
  width: 100vw;
  height: 100vh;
}
</style>