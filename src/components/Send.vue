<template>
    <div class="text-center">
      <v-btn

        @click="snackbar = true"
         v-ripple

          class="white--text"
          color="grey darken-3"
          form action="mailto:kym.nazim@gmail.com" method="post" enctype="text/plain"
      >
        Send
      </v-btn>

      <v-snackbar
        v-model="snackbar"
        :timeout="timeout"
      >
        {{ text }}

        <template v-slot:action="{ attrs }">
          <v-btn
            color="green"
            text
            v-bind="attrs"
            @click="snackbar = false"
          >
            Close
          </v-btn>
        </template>
      </v-snackbar>
    </div>
</template>

<script>
   export default {
     name: 'Send',
    data: () => ({
    snackbar: false,
    text: 'Message Sent',
    timeout: 2000,
  }),
   }
</script>
<style scoped>
</style>
