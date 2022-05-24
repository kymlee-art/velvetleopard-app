<template>
  <v-carousel hide-delimiters>
    <v-carousel-item
      v-for="(item,i) in items"
      :key="i"
      :src="item.src"
      reverse-transition="fade-transition"
      transition="fade-transition"
      :height="imageHeight"
    >

      <v-card-text class="text-center">
        <v-row>
          <v-col>
            <h2 class="mt-6 pt-6">BOLD</h2>
            <p class="bold">
              Creatively Different</p></v-col></v-row>
      </v-card-text>
        <v-card-action class="d-inline pa-2 mx-auto">

          <v-row>
            <v-col>

          <Buy class="mx-auto"></Buy></v-col>
          <v-col>
          <DialogTry class="mx-auto"></DialogTry></v-col>
           </v-row>

          </v-card-action></v-carousel-item>

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
