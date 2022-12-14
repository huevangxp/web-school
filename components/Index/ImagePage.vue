<template>
  <v-container fluid>
    <v-row>
      <v-col v-for="data in [1, 2, 3]" :key="data" cols="12" md="3">
        <v-card elevation="1" >
          <v-card-text>
            <v-img
              src="https://thethemedemo.b-cdn.net/educat/wp-content/uploads/2021/05/2.png"
            ></v-img>
          </v-card-text>
          <v-card-text> Teacher Uncle </v-card-text>
        </v-card>
      </v-col>
    </v-row>
    <v-card class="d-flex">
  <v-spacer/>
<v-btn color="primary" to="/teacher">More Teacher <v-icon class="ml-2">mdi-arrow-right</v-icon></v-btn>
</v-card>
  </v-container>
</template>

<script>
export default {
  name: 'ImagePage',
}
</script>
