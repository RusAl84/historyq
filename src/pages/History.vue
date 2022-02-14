<template>
  <yandex-map :coords="coords" :settings="settings">
      <ymap-marker
        marker-id="1"
        :coords="coords2"
        :marker-events="['click']"
      ></ymap-marker>
      <ymap-marker
        marker-id="2"
        :coords="coords1"
        :marker-events="['click']"
      ></ymap-marker>
    </yandex-map>
</template>

<script>
import { yandexMap, ymapMarker } from 'vue-yandex-maps'
export default {
  name: 'App',
  components: { yandexMap, ymapMarker },
  setup() {
    return {
      coords: [58, 39],
      coords1: [58, 39],
      coords2: [59, 39],
      settings : {
        apiKey: '73784db1-80df-448a-95a3-6f81554055ea',
        lang: 'ru_RU',
        coordorder: 'latlong',
        enterprise: false,
        version: '2.1'
    }
    }
  }
}
</script>

<style>
.ymap-container {
  height: 600px;
}
</style>
