<template>
  <v-container fluid>
    <div class="mx-auto">
      <v-card-title> ຫົວໜ້າ ຮຮ </v-card-title>
    </div>
    <v-card max-width="300" class="mx-auto" hover to="/teacher/_id">
      <v-card-text>
        <v-img
          class="pa-10"
          src="https://sites.ed.gov/hispanic-initiative/files/2014/09/hector_ibarra_pic01.jpg"
        ></v-img>
      </v-card-text>
      <v-card-title class="d-flex justify-center" >Teacher Mike
      </v-card-title>

      <v-divider />
    </v-card>
    <div>
      <v-card-title> ຮອງ ຫົວໜ້າ ຮຮ </v-card-title>
      <v-divider />
    </div>
    <v-row>
      <v-col
        v-for="data in [1, 2, 3]"
        :key="data"
        cols="12"
        md="3"
        class="mx-auto"
      >
        <v-card max-width="300" hover class="mb-10 mt-3 mx-auto">
          <v-card-text>
            <v-img
              class="pa-10"
              src="https://sites.ed.gov/hispanic-initiative/files/2014/09/hector_ibarra_pic01.jpg"
            ></v-img>
          </v-card-text>
          <v-card-title class="d-flex justify-center">Teacher Mike
          </v-card-title>
        </v-card>
      </v-col>
    </v-row>
    <v-divider />
    <div>
      <v-card-title> All Teacher</v-card-title>
      <v-divider />
    </div>
    <v-row>
      <v-col
        v-for="data in [1, 2, 3,4,5,6,7,8,9,10,11,12]"
        :key="data"
        cols="12"
        md="3"
        class="mx-auto"
      >
        <v-card max-width="300" hover class="mb-10 mt-3 mx-auto">
          <v-card-text>
            <v-img
              class="pa-10"
              src="https://sites.ed.gov/hispanic-initiative/files/2014/09/hector_ibarra_pic01.jpg"
            ></v-img>
          </v-card-text>
          <v-card-title class="d-flex justify-center"
            >Teacher Mike
          </v-card-title>
        </v-card>
      </v-col>
    </v-row>
    <v-divider />
  </v-container>
</template>

<script>
export default {
  name: 'Teacher',
}
</script>
