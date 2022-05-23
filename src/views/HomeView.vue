<template>
<v-content id="hero" color= "#DEBA27">
 <v-responsive
    class="mx-auto mb-12"
    width="100vw"

  >
        <v-row no-gutters>
          <v-img
            display="inline-block"
            height="300"

            justify content=centre
            :min-height="'calc(100vh - ' + $vuetify.application.top + 'px)'"
            src='../assets/velvet leopard.png'
            alt="logo"
            contain></v-img>

            <v-theme-provider dark>
              <v-container
            fill-height

              >
                <v-row
                  class="black--text mx-auto"
                  justify="center"

                >
                  <!-- <v-btn
                    class="align-self-end"
                    fab

                    font-black

                  > -->
                    <v-icon
                    color="black"
                    x-large
                    @click="$vuetify.goTo('#carousel')"
                    >mdi-chevron-down</v-icon>

                </v-row>
              </v-container>
            </v-theme-provider>
          </v-img>
        </v-row>
</v-responsive>


<!------- CAROUSEL -------------->

        <section id="carousel" class="white mt-2" >
<Carousel>
  <v-card>
  <Buy></Buy>
  <DialogBuy></DialogBuy>
  </v-card>
</Carousel>
            </section>

<!-- parallax -->
          <v-parallax
            :height="$vuetify.breakpoint.smAndDown ? 700 : 500"
            src="../assets/women5.png"
            >
          <v-container fill-height>
            <v-row class="mx-auto">
              <v-col
                :key="title"
                cols="12"
                md="3"
              >
              </v-col>
            </v-row>
          </v-container>
        </v-parallax>

<v-spacer></v-spacer>


<!-- Info-->
<info-view></info-view>

<!------------------- ABOUT------------- -->
<about-view></about-view>

<!-- Video-->
<!-- cant seem to get video going -->
<section id="video" class="mx-auto white">

<v-container>
  <v-layout>
    <v-flex> <v-row
        class="mb-4"
        no-gutters
      >

          <v-card
            class="mx-auto mt-16 ml-8 mr-8 pa-2 text-center"

          >
            Presenting Velvet Leopard's Motion Graphic Video
            Show-casing the unqiue and diversive style, for thoose that love to be different!

          </v-card>

     <v-row>
          <v-card
            class="pa-2 mx-auto text-center"
            outlined
            tile
          >

          <Video></Video>VIDEO GOES HERE
          </v-card>
        </v-row>

        </v-col>
      </v-row>
      <v-row no-gutters>

      </v-row></v-flex>
  </v-layout>

</v-container>

</section>


<!-- CONTACT --cannot seemt to import my contact page or component (both same) so I can delete it here---->

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

        </v-checkbox>
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


<!------------ FOOTER ---------------->
<Footer></Footer>
</v-content>
</template>


<script>
import Carousel from '../components/Carousel.vue'
import DialogTry from '../components/DialogTry.vue'
import Buy from '../components/Buy.vue'
import Video from '../components/Video.vue'
import MessageDialog from '../components/Video.vue'
import Cart from '../components/Cart.vue'
import AboutView from '../views/AboutView.vue'
import Footer from '../components/Footer.vue'
import InfoView from './InfoView.vue'
import ContactView from './ContactView.vue'







  export default {
  components: { Carousel, DialogTry, Buy, MessageDialog, Video, AboutView, Footer, Cart, InfoView},
    data () {
      return {
          message: 'Far far away, behind the word mountains, far from the countries Vokalia and Consonantia, there live the blind texts',
          dialog: false,
          email: undefined,
          form: false,
          isLoading: false,
          name: undefined,
          phone: undefined,
          rules: {
            email: v => !!(v || '').match(/@/) || 'Please enter a valid email',
            length: len => v => (v || '').length >= len || `Invalid character length, required ${len}`,
            required: v => !!v || 'This field is required',
          },

        // items: [
        //   {
        //     src: "../assets/ear2.png",
        //   },
        //   {
        //     src: '../assets/ear3.png',
        //   },
        //   {
        //     src: '../assets/ear4.png',
        //   },
        //   {
        //     src: '../assets/ear5.png',
        //   },
        //    {
        //     src: '../assets/ear6.png',
        //   },
        //    {
        //     src: '../assets/ear7.png',
        //   },
        //    {
        //     src: '../assets/earings/earings1.png',
        //   },
        // ],
      justify: [
        'start',
        'center',
        'end',
        'space-around',
        'space-between',
      ],
      computed: {
      cols () {
        const { lg, sm } = this.$vuetify.breakpoint
        return lg ? [3, 9] : sm ? [9, 3] : [6, 6]
      },
    },
      imageHeight () {
        switch (this.$vuetify.breakpoint.name) {
          case 'xs': return '200px'
          case 'sm': return '400px'
          case 'md': return '600px'
          case 'lg': return '800px'
          case 'xl': return '1000px'
        }
      },
      }
    },
  }
</script>

<style scoped>
#hero{
  background-color: #DEBA27;
}
#about-banner{
  left: 10rem;
  top:10rem;
  position: absolute;
}

.theme--dark.v-btn.v-btn--icon {
    color: #424242;
    width: 20;
}
</style>

