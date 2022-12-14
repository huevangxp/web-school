<template>
  <v-container fluid>
    <v-row>
      <v-col v-for="data in [1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16,17,18,19,20,21,22,23,24]" :key="data" cols="12" md="2">
        <v-card elevation="0" raised>
            <v-img src="https://thethemedemo.b-cdn.net/educat/wp-content/uploads/2021/06/course-6-500x300.jpg"></v-img>
        </v-card>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
    name:'ImagePage'
}
</script>
