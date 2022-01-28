<template>
  <div class="row map">
    <l-map :zoom="zoom" :center="center">
      <l-tile-layer :url="url" :attribution="attribution"></l-tile-layer>
      <!--
      <l-marker :lat-lng="marker2">
          <l-tooltip>Hello!</l-tooltip>
      </l-marker>
        -->

      <l-marker v-for="stanica in stanice" :key="stanica.id" :lat-lng="latLon(stanica.lat, stanica.lon)"> <l-popup>{{stanica.tags.name}}</l-popup></l-marker>
        
    </l-map>
  </div>
</template>

<script>

import L from 'leaflet';
import { LMap, LTileLayer, LMarker, LPopup } from 'vue2-leaflet';

import stanice from "../assets/stanice.JSON";

export default {
    name: "karta",
    data() {
    return {
      zoom:14,
      center: L.latLng(44.194, 17.9105),
      url:'https://tile.thunderforest.com/transport-dark/{z}/{x}/{y}.png?apikey=697b5f912cab4db88b43ccf0cde53f7c',
      attribution:'&copy; <a href="http://osm.org/copyright">OpenStreetMap</a> contributors',
      marker: L.latLng(47.413220, -1.219482),
      marker2: L.latLng(44.1519725, 17.9612504),

      stanice: stanice,
    }
    },
    methods:{
        latLon: function(lat, lon){
            return L.latLng(lat, lon)
        }
    },

    components: {
        LMap,
        LTileLayer,
        LMarker,
        
        LPopup
    },
    

}


</script>





<style>

.map{
    height: 95vh;
}

</style>