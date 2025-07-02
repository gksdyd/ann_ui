<template>
  <router-view />
</template>
<script>
import { onMounted } from 'vue';
import {useSetting} from './store/pinia'

export default {
  name: 'App',
  setup(){
    const store = useSetting()
    onMounted(()=>{
      store.setSetting()
    })
  }
}
</script>

<style lang="scss">
// @import "./assets/scss/socialv.scss";
@import "./assets/scss/customizer.scss";
@import "./assets//scss/custom.scss";
@import url("./plugins/Leaflet/leaflet.css");
@import url("./plugins/fullcalendar/core/main.css");
@import url("./plugins/fullcalendar/daygrid/main.css");
@import url("./plugins/fullcalendar/timegrid/main.css");
@import url("./plugins/fullcalendar/list/main.css");
</style>
