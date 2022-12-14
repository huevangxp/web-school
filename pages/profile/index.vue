<template>
  <v-container fluid>
    <v-row>
      <v-col cols="12" class="d-md-flex">
        <v-col cols="12" md="4">
          <v-card elevation="0">
            <v-card-title>
              <v-img
                src="https://media-exp1.licdn.com/dms/image/C4E03AQHYvufAPwei5Q/profile-displayphoto-shrink_800_800/0/1592953668313?e=2147483647&v=beta&t=ukv67Vcqls6yf4q52PWpOu9BBA1z8H_p1Q0MiXF_2GM"
              ></v-img>
            </v-card-title>
          </v-card>
        </v-col>
        <v-col cols="12" md="8">
          <v-card elevation="0">
            <v-card-title> Teacher Name </v-card-title>
            <v-card-text> Teach Class 4/3 </v-card-text>
            <v-card-text> Teache History </v-card-text>
            <v-card-text>
                Lorem ipsum dolor sit amet consectetur adipisicing elit. Sequi minus nemo, mollitia nisi ea reprehenderit, esse vero facilis voluptate, distinctio quibusdam eius obcaecati quos exercitationem. Similique officiis cupiditate suscipit veniam incidunt corporis eum possimus ea, amet ab minus enim deleniti quo dolores saepe soluta magni, mollitia cumque, sint reiciendis illum aut temporibus aliquid ipsa? Recusandae voluptates rerum facilis nisi maiores!
            </v-card-text>
            <v-row>
                <v-col v-for="data in [1,2,3]" :key="data" cols="12" md="3" class="mx-auto">
                    <v-card max-width="300">
                        <v-card-title>All Teacher And Student</v-card-title>
                        <v-card-title class="d-md-flex justify-md-center">5000 People</v-card-title>
                    </v-card>
                </v-col>
            </v-row>
          </v-card>
        </v-col>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {}
</script>
