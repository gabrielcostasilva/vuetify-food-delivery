<template>
  <v-navigation-drawer app color="grey lighten-3" right width="270">
    
    <v-toolbar color="grey lighten-3" flat>
      <v-spacer></v-spacer>
      <v-btn icon>
        <v-badge bordered overlap color="red" dot>
          <v-icon>fas fa-bell</v-icon>
        </v-badge>
      </v-btn>
      <v-badge bordered bottom color="green" dot offset-x="10" offset-y="10">
        <v-avatar size="40" rounded>
          <v-img src="https://cdn.vuetifyjs.com/images/lists/2.jpg"></v-img>
        </v-avatar>
      </v-badge>
      <v-btn icon>
        <v-icon>fas fa-ellipsis-v</v-icon>
      </v-btn>
    </v-toolbar>
    
    <MyOrder />
    
    <v-divider></v-divider>

    <Shopcart />

    <PaymentWidget />

  </v-navigation-drawer>
</template>

<script>
import MyOrder from './MyOrder.vue'
import Shopcart from './Shopcart.vue'
import PaymentWidget from './PaymentWidget.vue'

export default {
  components: {
    MyOrder,
    Shopcart,
    PaymentWidget
  }
}
</script>
