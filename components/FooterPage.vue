<template>
   <v-container fluid>
    <template>
  <v-footer
    dark
    color="primary"
    padless
  >
    <v-card
      class="flex"
      flat
      tile
    >
      <v-card-title class="primary">
        <strong class="subheading">Get connected with us on social networks!</strong>

        <v-spacer></v-spacer>

        <v-btn
          v-for="icon in icons"
          :key="icon"
          class="mx-4"
          dark
          icon
        >
          <v-icon size="24px">
            {{ icon }}
          </v-icon>
        </v-btn>
      </v-card-title>

      <v-card-text class=" primary py-2 white--text text-center">
        {{ new Date().getFullYear() }} — <strong>TAMIXAY SCHOOL</strong>
      </v-card-text>
    </v-card>
  </v-footer>
</template>
   </v-container>
  </template>
  <script>
  export default {
    data: () => ({
      icons: [
        'mdi-facebook',
        'mdi-twitter',
        'mdi-linkedin',
        'mdi-instagram',
      ],
    }),
  }
</script>