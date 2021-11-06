<template>
  <div>
    <v-container>
      <ShopcartItem
        v-for="(shopcartItem, index) in shopcartItems"
        :key="index"
        :picture="shopcartItem.mealPicture"
        :mealName="shopcartItem.mealName"
        :mealWeight="shopcartItem.mealWeight"
        :mealPrice="shopcartItem.mealPrice"
        :mealQuantity="shopcartItem.mealQuantity"
      />
    </v-container>

    <div class="text-center">
      <v-btn class="px-12" outlined color="green">Drag & Drop</v-btn>
    </div>

    <v-toolbar class="pl-0" flat color="grey lighten-3">
      <h3>Total</h3>
      <v-spacer></v-spacer>
      <h3>{{ shopcartTotal }}</h3>
    </v-toolbar>

    <div class="text-center">
      <v-btn class="px-15" rounded color="green" dark> Checkout </v-btn>
    </div>
  </div>
</template>

<script>
import ShopcartItem from './ShopcartItem'

export default {
  components: {
    ShopcartItem,
  },
  computed: {
    shopcartTotal() {
      return this.shopcartItems
        .map((currentItem) => currentItem.mealPrice)
        .reduce((previousValue, currentValue) => previousValue + currentValue)
    },
  },
  data() {
    return {
      shopcartItems: [
        {
          mealName: 'Bean soup',
          mealWeight: '350g',
          mealPrice: 4.2,
          mealPicture: '0.png',
          mealQuantity: 1,
        },
        {
          mealName: 'Noodle salad',
          mealWeight: '300g',
          mealPrice: 6.3,
          mealPicture: '6.png',
          mealQuantity: 1,
        },
        {
          mealName: 'Roast potato',
          mealWeight: '350g',
          mealPrice: 4.99,
          mealPicture: '3.png',
          mealQuantity: 1,
        },
      ],
    }
  },
}
</script>
