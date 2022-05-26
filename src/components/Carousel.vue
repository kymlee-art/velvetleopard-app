<template>
  <v-carousel hide-delimiters>
    <v-carousel-item
      v-for="(item,i) in items"
      :key="i"
      :src="item.src"
      reverse-transition="fade-transition"
      transition="fade-transition"

    >

      <v-card-text class="text-center">
        <v-row>
          <v-col>
            <h2 class="mt-6">BOLD</h2>
            <p class="bold">
              Creatively Different</p></v-col></v-row>
      </v-card-text>
   </v-carousel-item>

  </v-carousel>
</template>


<script>
  export default {
    name: 'Carousel',
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
  }
</script>
<style scoped>
.v-carousel__controls{
  background-color: white;
}
.v-item-group{
  color: black;
}
</style>
