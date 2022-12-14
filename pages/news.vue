<template>
  <v-container fluid>
    <!-- <v-row>
      <v-col cols="12" md="8" class="mx-auto"> -->
        <NewsPage />
      <!-- </v-col>
      <v-col cols="12" md="4">
          <v-app fixed app>
            <v-time-picker
            v-model="picker"
            :landscape="$vuetify.breakpoint.smAndUp"
            no-title
            size="300"
          ></v-time-picker>
          </v-app>
      </v-col>
    </v-row> -->
  </v-container>
</template>

<script>
export default {
  name: 'NewPage',
  data() {
    return {
      picker: null,
    }
  },
}
</script>
