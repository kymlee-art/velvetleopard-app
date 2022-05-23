<template>
   <div class="text-center">
      <v-dialog
        v-model="dialog"
        width="400"
      >
        <template v-slot:activator="{ on, attrs }">
          <v-btn
            color="grey darken-3"
            dark
            v-bind="attrs"
            v-on="on"
          >
            Send
          </v-btn>
        </template>

        <v-card
                color="grey darken-2">
          <v-card-title class="text-h5 white--text">
            Success
          </v-card-title>

          <v-card-text>
           Your Message Has Been Sent...
          </v-card-text>

          <v-divider></v-divider>

          <v-card-actions>
            <v-spacer></v-spacer>
            <v-btn
              color="white"
              text
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
     name: 'MessageDialog',
    data () {
    return {
      name: MessageDialog,
      MessageDialog: false,

    }
  },
   }
</script>
