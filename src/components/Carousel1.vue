<template>
     <v-sheet
    class="mx-auto"
    elevation="8"
    max-width="800"
  >
    <v-slide-group
      v-model="model"
      class="pa-4"
      active-class="success"
      show-arrows
    >
      <v-slide-item
        v-for="n in 15"
        :key="n"
        v-slot="{ active, toggle }"
         :src="item.src"
      >
        <v-card
          :color="active ? undefined : 'grey lighten-1'"
          class="ma-4"
          height="200"
          width="100"
          @click="toggle"
        >
          <v-row
            class="fill-height"
            align="center"
            justify="center"
          >
            <v-scale-transition>
              <v-icon
                v-if="active"
                color="white"
                size="48"
                v-text="'mdi-close-circle-outline'"
              ></v-icon>
            </v-scale-transition>
          </v-row>
        </v-card>
      </v-slide-item>
    </v-slide-group>
  </v-sheet>

</template>

<script>
 export default {
    name: 'Carousel1',

    data () {

		return {
      items: [
          {
            src: require('../assets/earings/earing1.png'),
          },
          {
            src: require('../assets/earings/earing2.png'),
          },
          {
            src: require('../assets/earings/earing3.png'),
          },
           {
            src: require('../assets/earings/earing4.png'),
          },
          {
            src: require('../assets/earings/earing5.png'),
          },
           {
            src: require('../assets/earings/earing6.png'),
          },
           {
            src: require('../assets/earings/earing7.png'),
          },

        ],

		}
  },
  computed: {
    columns() {
      if (this.$vuetify.breakpoint.xl) {
        return 4;
      }

      if (this.$vuetify.breakpoint.lg) {
        return 3;
      }

      if (this.$vuetify.breakpoint.md) {
        return 2;
      }

      return 1;
    }
  },
}
</script>

