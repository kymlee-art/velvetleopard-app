<template>
  <v-app id="main-section">
     <v-navigation-drawer
     v-model="drawer"
     app
     >
      <v-list-item>
        <v-list-item-content>
          <v-list-item-title class="text-h6">
            Velvet Leopard
          </v-list-item-title>
          <v-list-item-subtitle>
            Designs that Attract
          </v-list-item-subtitle>
        </v-list-item-content>
      </v-list-item>

      <v-divider></v-divider>

      <v-list
        dense
        nav
        text-right

      >
        <v-list-item
          v-for="item in items"
          :key="item.title"
          :to="item.to"
          link
        >
          <v-list-item-icon>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-item-icon>

          <v-list-item-content>
            <v-list-item-title>{{ item.title }}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>

  <div>
    <v-app-bar
      app
      color="#DEBA27"
      dense
      flat
    >
      <v-app-bar-nav-icon @click="drawer=!drawer"></v-app-bar-nav-icon>
      <v-spacer></v-spacer>

      <v-tab class="pa-4 font-weight-black"
        centered
        background-color="transparent"
        @click="$vuetify.goTo('#hero')"
      >
        Home
      </v-tab>
      <v-tab class="pa-4 font-weight-black"
        centered
        background-color="transparent"
        @click="$vuetify.goTo('#about')"
      >
        About
      </v-tab>

      <v-tab class="pa-4 font-weight-black "
      text
      @click="$vuetify.goTo('#carousel')">
        Gallery
      </v-tab>

      <v-tab class="pa-4 font-weight-black "
      to="#contact"
      text
      @click="$vuetify.goTo('#contact')"
      >
        Contact
      </v-tab>


<!-- CART BUTTON / DIALOG POPUP -->
<Cart <v-btn icon>
        <v-icon
        >mdi-basket-outline</v-icon>
      </v-btn></Cart>

      <v-menu
        left
      >

        <v-list>
          <v-list-item
            v-for="n in 5"
            :key="n"
            @click="$vuetify.goTo('#')"
          >
            <v-list-item-title>Option {{ n }}</v-list-item-title>
          </v-list-item>
        </v-list>
      </v-menu>
    </v-app-bar>
  </div>


     <v-main>
        <router-view></router-view>

    </v-main>

  </v-app>
</template>







<script>
import Cart from '../src/components/Cart.vue'

  export default {
    components: {Cart},
    data: () => ({
          drawer: false,
    }),
         items: [
          { title: 'Home', icon: 'mdi-home-outline', to: '/' },
          { title: 'About', icon: 'mdi-information-variant', goTo: '#about' },
          { title: 'Gallery', icon: 'mdi-view-dashboard', goTo: '#gallery' },
          { title: 'Contact', icon: 'mdi-email-edit-outline', goTo: '#contact' },
        ],

  }

</script>

<style scoped>
.v-application a {
    color: black;
    font-style: normal;
    text-decoration-line: none;
}
</style>

