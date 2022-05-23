<template>
  <v-carousel>
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
            <h2>BOLD</h2>
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
            src: '../assets/earings/ear2.png', alt:"earings",
          },
          {
            src: 'https://cdn.vuetifyjs.com/images/carousel/sky.jpg',
          },
          {
            src: 'https://cdn.vuetifyjs.com/images/carousel/bird.jpg',
          },
          {
            src: 'https://cdn.vuetifyjs.com/images/carousel/planet.jpg',
          },
        ],

      }
    },
  }
</script>
