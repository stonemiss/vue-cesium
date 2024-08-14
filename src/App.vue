<script setup>
import * as Cesium from 'cesium';
import { onMounted } from "vue";
onMounted(() => {

  const viewer = new Cesium.Viewer('cesiumContainer', {
    imageryLayers: new Cesium.ArcGisMapServerImageryProvider({
      name: "img_arcgis",
      url: "https://services.arcgisonline.com/ArcGIS/rest/services/World_Imagery/MapServer"
    }),
    // baseLayer: new Cesium.ImageryLayer.fromProviderAsync(
    //   Cesium.IonImageryProvider.fromAssetId(3812)
    // ),
    baseLayerPicker: false,
    // skyBox: new Cesium.SkyBox({
    //   sources: {
    //     positiveX: "stars/TychoSkymapII.t3_08192x04096_80_px.jpg",
    //     negativeX: "stars/TychoSkymapII.t3_08192x04096_80_mx.jpg",
    //     positiveY: "stars/TychoSkymapII.t3_08192x04096_80_py.jpg",
    //     negativeY: "stars/TychoSkymapII.t3_08192x04096_80_my.jpg",
    //     positiveZ: "stars/TychoSkymapII.t3_08192x04096_80_pz.jpg",
    //     negativeZ: "stars/TychoSkymapII.t3_08192x04096_80_mz.jpg"
    //   }
    // }),
  });

})
</script>

<template>
  <div id="cesiumContainer"></div>
</template>

<style scoped>
html,
body,
#cesiumContainer {
  width: 100%;
  height: 100%;
  margin: 0;
  padding: 0;
  overflow: hidden;
}
</style>
