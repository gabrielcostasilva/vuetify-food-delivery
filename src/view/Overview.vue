<template>
  <v-container>
    <v-toolbar flat>
      <v-row>
        <v-col cols="12" sm="10">
          <v-text-field
            label="Search"
            filled
            rounded
            dense
            solo
            flat
            background-color="grey lighten-3"
          ></v-text-field>
        </v-col>
        <v-col cols="12" sm="2">
          <v-btn> <v-icon>fas fa-filter</v-icon>Filter </v-btn>
        </v-col>
      </v-row>
    </v-toolbar>
    <v-row>
      <v-col cols="12" sm="6">
        <v-toolbar flat>
          <h5>My Filters:</h5>
          <v-icon class="ml-1" small>fas fa-car-side</v-icon>
          <h5 class="ml-1">First Meal</h5>
          <v-chip class="ma-2" color="green" text-color="white" dense>
            <v-avatar left>
              <v-icon>fas fa-running</v-icon>
            </v-avatar>
            After Training
          </v-chip>
          <v-spacer></v-spacer>
          <h6 class="green-text">ADD</h6>
        </v-toolbar>
      </v-col>
      <v-col cols="12" sm="6">
        <v-toolbar flat>
          <h5>Popular Filters:</h5>
          <v-icon class="ml-1" small>fas fa-child</v-icon>
          <h5 class="ml-1">Slim Waist</h5>
          <v-spacer></v-spacer>
          <v-icon class="ml-1" small>fas fa-birthday-cake</v-icon>
          <h5 class="ml-1">Diet</h5>
        </v-toolbar>
      </v-col>
    </v-row>
    <v-toolbar class="pl-0 mt-n7" flat>
      <h4>345</h4>
      <h4 class="grey--text text-lighten-1 ml-2">Meals found</h4>
      <v-spacer></v-spacer>
      <h4 class="grey--test text-lighten-1">Sorted by:</h4>
      <h4 class="ml-1">Recommended</h4>
      <v-icon class="ml-1" small>fas fa-chevron-down</v-icon>
    </v-toolbar>
    <v-row class="mt-n6">
      <MealThumbnail
        v-for="(meal, i) in meals"
        :key="i"
        :stars="meal.stars"
        :picture="meal.picture"
        :mealName="meal.mealName"
        :mealWeight="meal.mealWeight"
        :mealPrice="meal.mealPrice"
        :colour="setColour(i)"
      />
    </v-row>

    <div class="d-flex flex-column justify-space-between align-center">
      <v-btn class="px-15 mt-2" rounded outlined color="green" dark>
        <v-icon class="mr-1"> fas fa-spinner </v-icon>
        Load More
      </v-btn>
    </div>
  </v-container>
</template>

<script>
import MealThumbnail from '../components/MealThumbnail.vue'

export default {
  components: {
    MealThumbnail,
  },
  methods: {
    setColour(index) {
      return index % 2 ? 'red lighten-5' : 'blue lighten-5'
    },
  },
  data() {
    return {
      meals: [
        {
          stars: 4.2,
          picture: '0.png',
          mealName: 'Cabage salad',
          mealWeight: '250g',
          mealPrice: 4.99,
        },
        {
          stars: 4.5,
          picture: '1.png',
          mealName: 'Noodle salad',
          mealWeight: '300g',
          mealPrice: 6.3,
        },
        {
          stars: 5.0,
          picture: '3.png',
          mealName: 'Vegetable mix',
          mealWeight: '400g',
          mealPrice: 5.99,
        },
        {
          stars: 4.4,
          picture: '4.png',
          mealName: 'Sea food',
          mealWeight: '350g',
          mealPrice: 6.1,
        },
        {
          stars: 5.0,
          picture: '2.png',
          mealName: 'Bean soup',
          mealWeight: '300g',
          mealPrice: 4.3,
        },
        {
          stars: 4.7,
          picture: '8.png',
          mealName: 'Stewed vegetables',
          mealWeight: '400g',
          mealPrice: 4.99,
        },
      ],
    }
  },
}
</script>
