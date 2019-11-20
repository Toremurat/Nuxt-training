<template>
  <yandex-map
  :coords="[43.248910, 76.943910]"
  zoom="13"
  style="width: 100%; height: 600px;"
  :behaviors="['drag', 'scrollZoom']"
  :controls="['trafficControl']"
  map-type="map"
  id="map-fullscreen"
>
 
    <ymap-marker
      marker-id="1"
      :coords="[43.230151, 76.946073]"
      hint-content="Нурлы Тау"
      :icon="{color: 'red', glyph: 'Pocket'}"
    ></ymap-marker>
 
    <ymap-marker
      marker-id="2"
      :coords="[43.264204, 76.929861]"
      hint-content="Мега парк"
      :balloon="{header: 'Мега парк'}"
    ></ymap-marker>
 
</yandex-map>
</template>
<script>
export default {
//   data() {
//   return {
//     placemarks: [
//       {
//         coords: [54.8, 39.8],
//         properties: {}, // define properties here
//         options: {}, // define options here
        
//       }
//     ]
//   }
// }
}
</script>