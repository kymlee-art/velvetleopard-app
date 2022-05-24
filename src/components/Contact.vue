<template>

<section id="contact"
        class="#DEBA27">

 <v-container class=" ml-0 pa-0 ">

    <v-row no-gutters>
      <v-flex class="mx-auto">
         <v-col

         cols="#DEBA27">
        <v-img
        class="mx-auto"
        src="../assets/velvet leopard.png"
        width="400"
        justify="center">

        </v-img>
     <v-card
     id="contact-details"
     class="#DEBA27 mx-auto pl-16 mt-n16"
     color="#DEBA27"
     flat
     dense
     width="300"

     >
             <h2>Jacinta Campbell</h2>
             <p>1133 Delaware Drive Melbourne, Victora 3000</p>
             <p class="font-weight-black bold">Ph: 03 9333 2222</p>
             <div  class="d-flex" id="social-icons">
             <v-icon>mdi-facebook</v-icon>
             <v-icon>mdi-instagram</v-icon>
             <v-icon>mdi-linkedin</v-icon>
             <v-icon>mdi-twitter</v-icon>
             </div>
     </v-card>
        </v-col>
      </v-flex>
      <v-flex>
        <v-col cols="8" >
          <h2
          class="text-center mx-auto ml-15 mt-16 pa-16 font-weight-black"
          justify="center">Get in Touch!</h2>
   <v-card
      class="mx-auto  pl-10 pb-16"
      style="max-width: 600px; min-width: 300px;"
      color="#DEBA27"
      dense
      flat
    >

        <v-spacer></v-spacer>

      <v-form
        ref="form"
        v-model="form"
        class="pa-4 pt-6"
        color="#DEBA27"
      >
        <v-text-field
          filled
          color="teal accent-2"
          label="Name"
          style="min-height: 96px"
          type="text"
          solo
        ></v-text-field>
        <v-text-field
          v-model="phone"
          filled
          color="teal accent-2"
          label="Phone number"
          solo
        ></v-text-field>
        <v-text-field
          v-model="email"
          :rules="[rules.email]"
          filled
          color="teal accent-2"
          label="Email address"
          type="email"
          solo
        ></v-text-field>
        <v-textarea
          v-model="Message"
          auto-grow
          filled
          color="teal accent-2"
          label="Message"
          rows="1"
          solo
        ></v-textarea>


      </v-form>

      <v-card-actions>
        <v-btn
          text
          @click="$refs.form.reset()"
        >
          Clear
        </v-btn>
        <v-spacer></v-spacer>
        <v-btn
          v-ripple
          :loading="isLoading"
          class="white--text"
          color="grey darken-3"

        >
          Submit
        </v-btn>
      </v-card-actions>
      <v-dialog
        v-model="dialog"
        absolute
        max-width="600"
        persistent
      >
        <v-card>
          <v-card-title class="text-h5 ">
            Legal
          </v-card-title>
          <v-card-text>

          </v-card-text>

          <v-card-actions>
            <v-btn
              text
              @click="agreement = false, dialog = false"
            >
              No
            </v-btn>
            <v-spacer></v-spacer>

            <v-btn
              v-ripple
              class="black--text"
              color="teal darken-1"
              @click="agreement = true"
            >
              Yes
            </v-btn>
          </v-card-actions>
        </v-card>
      </v-dialog>
    </v-card>

        </v-col>
</v-flex>
      </v-row>
  </v-container>
</section>

</template>


<script>
   export default {
     name: 'Contact',
    data () {
    return {
      name: Contact,

    }
  },
   }
</script>
