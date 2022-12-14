<template>
  <v-container fluid>
    <v-card max-width="800" class="mx-auto" elevation="0">
        <v-card-title primary-title>
            Add Teacher to form
        </v-card-title>
        <v-card-text>
            <v-row>
                <v-col cols="12">
                    <v-text-field outlined dense hide-details="auto" placeholder="Teacher ID"></v-text-field>
                </v-col>
                <v-col cols="12" md="6">
                    <v-text-field outlined dense hide-details="auto" placeholder="Subject"></v-text-field>
                </v-col>
                <v-col cols="12" md="6">
                    <v-text-field outlined dense hide-details="auto" placeholder="Subject ID"></v-text-field>
                </v-col>
                <v-col cols="12" md="6">
                    <v-text-field outlined dense hide-details="auto" placeholder="Status"></v-text-field>
                </v-col>
                <v-col cols="12" md="6">
                    <v-text-field outlined dense hide-details="auto" placeholder="Reson"></v-text-field>
                </v-col>
                <v-col cols="12">
                    <v-textarea counter="25" outlined dense hide-details="auto" placeholder="Note by Subject ID"></v-textarea>
                </v-col>
            </v-row>
        </v-card-text>
        <v-card-actions>
            <v-btn color="red" dark width="100">Cancel</v-btn>
            <v-btn color="primary" width="100">Save</v-btn>
        </v-card-actions>
    </v-card>
  </v-container>
</template>

<script>
export default {

}
</script>
