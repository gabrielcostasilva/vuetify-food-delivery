<template>
  <div>
    <v-toolbar class="pl-0 mt-5" flat color="grey lighten-3">
      <h3>My Order</h3>
      <v-spacer></v-spacer>
      <h6 class="green--text">Edit</h6>
    </v-toolbar>
    <v-app-bar flat color="rgba(0, 0, 0, 0)" class="mt-n5">
      <v-btn fab x-small color="green lighten-4" elevation="0">
        <v-icon color="green">fas fa-clock</v-icon>
      </v-btn>
      <h5 class="ml-2 grey--text text--darken-2">14:30 AM</h5>
    </v-app-bar>
    <v-app-bar flat color="rgba(0, 0, 0, 0)" class="mt-n5">
      <v-btn fab x-small color="green lighten-4" elevation="0">
        <v-icon color="green">fas fa-map-marker-alt</v-icon>
      </v-btn>
      <h5 class="ml-2 grey--text text--darken-2">69 7th Ave-s, New York</h5>
    </v-app-bar>
    <v-app-bar flat color="rgba(0, 0, 0, 0)" class="mt-n5">
      <v-btn fab x-small color="green lighten-4" elevation="0">
        <v-icon color="green">fas fa-comment-dots</v-icon>
      </v-btn>
      <h5 class="ml-2 grey--text text--darken-2">
        Dial me for order specification
      </h5>
    </v-app-bar>
  </div>
</template>

<script>
export default {

}
</script>
