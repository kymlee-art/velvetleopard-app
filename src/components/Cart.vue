<template>
  <div class="text-center"
  >
  <v-menu
      v-model="menu"
      :close-on-content-click="false"
      :nudge-width="200"
      offset-x
      class="grey"


    >
      <template v-slot:activator="{ on, attrs }" class="grey">
        <v-icon
          color="black"
          v-bind="attrs"
          v-on="on"
        >mdi-basket-outline
        </v-icon>
      </template>

      <v-card id="cart-dialog"
      width="200"
      height="300"
      color="grey"


      >
        <v-list class="grey">
          <v-list-item><v-img

          src="../assets/velvet leopard.png"></v-img>
          <v-icon></v-icon>

            <v-list-item-content>
              <v-list-item-title>Your Cart</v-list-item-title>
              Your Cart is Empty
            </v-list-item-content>

            <v-list-item-action>

            </v-list-item-action>
          </v-list-item>
        </v-list>



        <v-list class="grey">
          <v-list-item>
            <v-list-item-action>

            </v-list-item-action>
            <v-list-item-title class="ml-n4">Coming Soon</v-list-item-title>
          </v-list-item>


        </v-list>

        <v-card-actions>
          <v-spacer></v-spacer>

          <v-btn
            text
            @click="menu = false"
          >
            Cancel
          </v-btn>
          <v-btn
            color="primary"
            text
            @click="menu = false"
          >
            Buy Now
          </v-btn>
        </v-card-actions>
      </v-card>
    </v-menu>
  </div>
</template>


<script>
   export default {
     name: 'Cart',
    data () {
    return {
      title: 'Cart',
      Cart: true,
      menu: false,
      title: 'menu',

    }
  },
   }
</script>
<style scoped>
.v-menu__content .v-menu, .card-dialog, .v-list-menu{
  background-color: grey;
}
.v-menu__content{
  background-color:rgba(128, 128, 128, 0.613);
}
</style>
