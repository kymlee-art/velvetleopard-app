<template>
  <v-app>
    <v-app-bar
      app
      color="primary"

    >
      <!-- <div class="d-flex align-center">
        <v-img
            alt="Velvet Leopard logo"
          class="shrink mr-2"
          contain
          src="./assets/velvet leopard.png"
          transition="scale-transition"
          width="40"
        /> -->

        <v-img
          alt="Velvet Leopard logo"
          class="shrink mt-1 hidden-sm-and-down"
          contain
          min-width="1000"
          src="./assets/velvet leopard.png"
          width="100"
        />
      </div>

      <v-spacer></v-spacer>

      <v-btn
        href="https://github.com/vuetifyjs/vuetify/releases/latest"
        target="_blank"
        text
      >
        <span class="mr-2">Latest Release</span>

      </v-btn>

    </v-app-bar>

    <v-main>
      <router-view/>
    </v-main>
  </v-app>
</template>

<script>
  export default {
name: 'Layout',
data () {
  return{
    label: 'Home',
    to: '/'
  }
}
  }
</script>


<style scoped>

</style>
