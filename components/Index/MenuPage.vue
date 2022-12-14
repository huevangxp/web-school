<template>
 <v-container fluid>
    <v-card
    elevation="0"
    >
        <v-row dense>
          <v-col cols="12">
            <v-card
              color="#385F73"
              dark
              class="d-md-flex"
            >
             <v-col cols="12" md="8">
                <v-card-text  class="text-h5">
                Welcome To TAMIXAY SCHOOL
              </v-card-text>
  
              <v-card-subtitle>
                Lorem, ipsum dolor sit amet consectetur adipisicing elit. Culpa nulla praesentium earum dicta doloribus, mollitia dolor incidunt rerum nisi aliquid deserunt facere impedit corrupti placeat libero! Exercitationem quo natus nisi reiciendis cupiditate neque culpa qui quidem, recusandae saepe repellat architecto debitis est voluptatibus dolore maiores voluptates. Expedita, iusto. Praesentium impedit accusamus modi illum assumenda possimus corporis, tenetur voluptates. Odio, alias animi assumenda explicabo quod esse nulla, tenetur nesciunt, accusamus beatae illum eius dignissimos officia laudantium similique eos. Hic laborum quae mollitia, illo commodi ea dolor, ullam dolores placeat quisquam eaque optio iste omnis ipsum error reiciendis modi tenetur, inventore voluptates.
              </v-card-subtitle>
  
              <v-card-actions>
                <v-btn text>
                  Listen Now
                </v-btn>
              </v-card-actions>
             </v-col>
             <v-col cols="12" md="4">
                <v-img 
                height="360"
                width="360"
                 src="/image.png"></v-img>
             </v-col>
            </v-card>
          </v-col>
  
        </v-row>
    </v-card>
 </v-container>
  </template>

<script>
export default {
  data: () => ({
    items: [
      {
        color: '#1F7087',
        src: 'https://cdn.vuetifyjs.com/images/cards/foster.jpg',
        title: 'Supermodel',
        artist: 'Foster the People',
      },
      {
        color: '#952175',
        src: 'https://cdn.vuetifyjs.com/images/cards/halcyon.png',
        title: 'Halcyon Days',
        artist: 'Ellie Goulding',
      },
    ],
  }),
}
</script>