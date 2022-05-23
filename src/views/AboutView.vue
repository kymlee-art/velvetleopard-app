<template>

<section id="about" class="white">
  <v-container class="  ml-0 pa-0 pt-16">

 <v-layout row wrap>
      <v-flex xs12 sm6>


          <v-img
          src='../assets/women.png'
          class="ml-16 mr-8"
          height="500px"

          ></v-img>
          <v-card
            color="#DEBA27"
            dense
             class="ma-16"
            width="500"
             :elevation="n - 1"
          >
          </v-card>

        </v-flex>
        <v-flex xs12 sm6>

          <v-card
            class="pa-2 "
            dense
            flat
             color="white"

          >
          <h2 class="text-center ml-15 pa-16 font-weight-black">Jacinta Campbell</h2>
<p class="pl-16 pb-6">
  Jacinta Campbell a talented and professional Jewellery Designer founded Velvet Leopard in 2020.
</p>
<p class="pl-16 pb-4">Her Designs feature the Uniqueness that every women strives for, setting trends and standing out, with her bold and funky creations that will add that special touch to any outfit.</p>
<p class="pl-16 pb-4">Velvet Leopard earrings are designed and made of high quality craftmanship with unique designs and the confidence of great style, and being daringly different!</p>
          </v-card>
        </v-flex>

 </v-layout>
  </v-container>

</section>
</template>

<script>
   export default {
     name: 'AboutView',
    data () {
    return {
      name: AboutView,

    }
  },
   }
</script>
