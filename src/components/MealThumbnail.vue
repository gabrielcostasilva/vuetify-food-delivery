<template>
  <v-col cols="12" sm="4">
    <v-hover v-slot="{ hover }" open-delay="200">
      <v-card :color="colour" :elevation="hover ? 16 : 2">
        <v-app-bar flat color="rgba(0, 0, 0, 0)">
          <v-chip class="ma-2" color="black" text-color="white" dense>
            <v-avatar left>
              <v-icon color="yellow">fas fa-star</v-icon>
            </v-avatar>
            {{ stars }}
          </v-chip>
          <v-spacer></v-spacer>
          <v-btn fab x-small color="white"><v-icon>fas fa-heart</v-icon></v-btn>
        </v-app-bar>
        <div class="d-flex flex-column justify-space-between align-center">
          <v-img :src="picture" max-height="180" max-width="180"></v-img>
        </div>
        <v-app-bar flat color="rgba(0, 0, 0, 0)">
          <h5 class="ml-1 grey--text text-lighten-3">{{ mealName }}</h5>
          <v-chip class="ma-2" color="grey lighten-3" text-color="red" dense>{{
            mealWeight
          }}</v-chip>
        </v-app-bar>
        <h5 class="ml-5 mt-n5">${{ mealPrice }}</h5>
      </v-card>
    </v-hover>
  </v-col>
</template>

<script>
export default {
  props: ['stars', 'picture', 'mealName', 'mealWeight', 'mealPrice', 'colour']
}
</script>

<style></style>
