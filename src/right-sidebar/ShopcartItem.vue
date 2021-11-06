<template>
  <v-row>
    <v-col cols="12" sm="3">
      <v-img
        :src="picture"
        max-height="50"
        max-width="50"
        contain
        class="mt-1 mr-1"
      ></v-img>
    </v-col>
    <v-col cols="12" sm="3">
      <h6 class="ml-n6 grey--text text-darken-2">
        {{ mealName }}<br />
        <span class="grey--text text-lighten-1">{{ mealWeight }}</span>
      </h6>
    </v-col>
    <v-col cols="12" sm="6">
      
      <IncreaseDecreaseButton :initValue="1" />

      <strong class="ml-1 mr-1">${{ mealPrice }}</strong>
      <v-icon x-small>fas fa-times</v-icon>
    </v-col>
  </v-row>
</template>

<script>
import IncreaseDecreaseButton from './IncreaseDecreaseButton.vue'

export default {
  components: {
    IncreaseDecreaseButton
  },
  props: ['picture', 'mealName', 'mealWeight', 'mealPrice', 'mealQuantity'],
}
</script>
