<template>
  <v-app>

    <v-app-bar
      app
      color="teal accent-2"
      dense
      flat
    >

      </v-img>

      <v-spacer></v-spacer>

      <v-btn
        to="/"
        target="_blank"
        text
      >
        <span class="ma-1">Home</span>

      </v-btn>
       <v-btn
        to="@/about"
        target="_blank"
        text
      >
        <span class="ma-1">About</span>

      </v-btn>
       <v-btn
         to="@/contact"
        target="_blank"
        text
      >


        <span class="ma-1" plain>Contact</span>
      </v-btn>
    </v-app-bar>

    <v-main class="main-1">

      <router-view/>
     <v-img
          alt="Velvet Leopard logo"
          class="hero-img"
          contain
          min-width="1000"
          src="./assets/velvet leopard.png"
          width="100"
        />
      </v-img>
      </v-main>
  </v-app>
</template>

<script>

export default {
  name: 'App',

  data: () => ({
    //
  }),
};
</script>

<style scoped>
.main-1{
background-color: #64FFDA;
}
</style>
