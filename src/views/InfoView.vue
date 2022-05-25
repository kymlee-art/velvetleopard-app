<template>
  <section id="info"  class="mx-auto #DEBA27"
  height="200">

<v-container>
  <v-layout>
    <v-flex>

    <v-row
        class="mb-4 mx-auto text-center"
        no-gutters
      >
        <v-col
          sm="2"
          md="4"
        ><v-card
        width="200px"
        class="pa-7  d-inline-block"
        color="#DEBA27"
        flat
        ><v-icon
        x-large
        color="green">
        mdi-palette-outline
        </v-icon>

        <p class="font-weight-black"
        >CREATIVE</p>
        <p>All designs are crafted to the highest standards. Designs that add flair</p>
        </v-card>

        </v-col>
        <v-col
          sm="2"
          md="4"
        >
          <v-card
            class="pa-7  d-inline-block"
            width="200px"
            color="#DEBA27"
            flat

          ><v-icon x-large color="black"> mdi-flower-pollen</v-icon>
        <p class="font-weight-black">BOLD</p><p>For that extra special touch that makes any outfit stand out</p>
          </v-card>
        </v-col>
         <v-col
          sm="2"
          md="4"
        >
          <v-card
            class="pa-7  d-inline-block"
            color="#DEBA27"
            width="200px"
            flat
          > <v-icon large color="orange">mdi-leaf</v-icon>
          <p class="font-weight-black">UNIQUE</p>
          <p>Be darinly Different, add that pop of colour and own your style!</p>


          </v-card>
        </v-col>
      </v-row>
      <v-row no-gutters>

      </v-row></v-flex>
  </v-layout>

</v-container>

</section>
</template>

<script>
   export default {
     name: 'InfoView',
    data () {
    }
   }
</script>
