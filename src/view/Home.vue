<template>
  <v-app id="inspire">
    <SideBarLeft />
    <SideBarRight />
    <Overview/>
  </v-app>
</template>

<script>
import SideBarLeft from '../components/SideBarLeft.vue'
import SideBarRight from '../right-sidebar/SideBarRight.vue'
import Overview from './Overview.vue'

export default {
  components: {
    SideBarLeft,
    SideBarRight,
    Overview
  },
}
</script>

<style></style>
