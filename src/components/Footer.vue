<template>
   <v-footer
    class="grey darken-3"
    dark
    padless
  >
    <v-card
      flat
      tile
      class="grey darken-3 black--text text-center mx-auto"
    >
      <v-card-text>
        <v-btn
          v-for="icon in icons"
          :key="icon"
          class="mx-4 white--text"
          icon
        >
          <v-icon size="24px">
            {{ icon }}
          </v-icon>
        </v-btn>
      </v-card-text>

      <v-card-text class="white--text pt-0"

      fill
      >
        Velvet Leopard was built as a project with fictional characters and names.
            All rights Reserved 2022
      </v-card-text>

      <v-divider></v-divider>

      <v-card-text class="white--text">
        {{ new Date().getFullYear() }} — <strong>Vuetify</strong>
      </v-card-text>
    </v-card>
  </v-footer>
</template>


<script>
   export default {
     name: 'Footer',
    data () {
    return {
      name: Footer,

    }
  },
   }
</script>
