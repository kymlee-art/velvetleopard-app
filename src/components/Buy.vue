  <template><div class="text-center">
      <v-dialog
      class="Buy"
        v-model="dialog"
        width="400"
      >
        <template v-slot:activator="{ on, attrs }">
          <v-btn
            color="teal accent-2"
            dark
            v-bind="attrs"
            v-on="on"
          >
           Buy
          </v-btn>
        </template>

        <v-card
        style="opacity: 0.8"
        color="teal lighten-2"
        class="mx-auto"
        height="300"
         centered

         >
          <v-img
          height="150px"
          width="150px"
          class="mx-auto buy-logo"
          src='../assets/velvet leopard.png'
          alt="logo">
          </v-img>

          <v-card-title
          class="mx-auto text-h5"
          color="primary">
          Success!
          </v-card-title>

          <v-card-text>
          <h3 >Added to Cart</h3>
          </v-card-text>
          <v-divider></v-divider>

          <v-card-actions>
            <!-- <v-spacer></v-spacer> -->

            <v-btn
              color="primary"
              text
              align="bottom"
              @click="dialog = false"
            >
            Close
            </v-btn>
          </v-card-actions>
        </v-card>
      </v-dialog>
    </div>
    </template>

<script>
   export default {
     name: 'Buy',
    data () {
    return {
     Buy: true,

    }
  },
   }
</script>

<style scoped>

</style>
