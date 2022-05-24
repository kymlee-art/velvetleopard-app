  <template><div class="text-center">
      <v-dialog
      class="DialogTry"
        v-model="dialog"
        width="300"
         height="300"
      >
        <template v-slot:activator="{ on, attrs }">
          <v-btn
            color="grey darken-2"
            dark
            v-bind="attrs"
            v-on="on"
            width="70"
          >
           Try On
          </v-btn>
        </template>

       <v-card
        style="opacity: 0.8"
        color="grey lighten-2"
        class="mx-auto"
        width="400"
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


          <v-card-text class="text-center font-weight-medium text-h5">
         Try-On - Comming Soon!
          </v-card-text>

          <v-card-actions>
            <v-spacer></v-spacer>
            <v-btn
              color="teal darken-2"
              text
                   align="bottom"
              @click="dialog = false"
            >
              Buy Now
            </v-btn>
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
     name: 'DialogTry',
    data () {
    return {
      DialogTry: false,
      dialog: false,
      tryOn: true,
    }
  },
   }
</script>
