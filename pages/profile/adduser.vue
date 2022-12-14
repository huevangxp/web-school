<template>
  <v-container fluid>
   <v-card  elevation="0" max-width="800" class="mx-auto">
    <v-card-title class="d-md-flex justify-md-center">Add Student to this form</v-card-title>
    <v-row>
            <v-col cols='12' >
                <v-text-field outlined dense placeholder="Student ID" hide-details="auto"></v-text-field>
            </v-col>
            <v-col cols='12'  md="6" >
                <v-text-field outlined dense placeholder="First Name" hide-details="auto"></v-text-field>
            </v-col>
            <v-col cols='12' md="6">
                <v-text-field outlined dense placeholder="Last Name" hide-details="auto"></v-text-field>
            </v-col>
            <v-col cols='12' md="6">
                <v-text-field outlined dense placeholder="Nick Name" hide-details="auto"></v-text-field>
            </v-col>
            <v-col cols='12' md="6">
                <v-text-field outlined dense placeholder="Age" hide-details="auto"></v-text-field>
            </v-col>
            <v-col cols='12' md="6">
                <v-text-field outlined dense placeholder="Telephone" hide-details="auto"></v-text-field>
            </v-col>
            <v-col cols='12' md="6">
                <v-text-field outlined dense placeholder="Position" hide-details="auto"></v-text-field>
            </v-col>
            <v-col cols='12' md="6">
                <v-text-field outlined dense placeholder="ClassNo" hide-details="auto"></v-text-field>
            </v-col>
            <v-col cols='12' md="6">
                <v-text-field outlined dense placeholder="Nice Score" hide-details="auto"></v-text-field>
            </v-col>
            <v-col cols='12' md="6">
                <v-text-field outlined dense placeholder="Farther Name" hide-details="auto"></v-text-field>
            </v-col>
            <v-col cols='12' md="6">
                <v-text-field outlined dense placeholder="Farther Phone" hide-details="auto"></v-text-field>
            </v-col>
            <v-col cols='12' md="6">
                <v-text-field outlined dense placeholder="Mother Name" hide-details="auto"></v-text-field>
            </v-col>
            <v-col cols='12' md="6">
                <v-text-field outlined dense placeholder="Mother Phone" hide-details="auto"></v-text-field>
            </v-col>
            <v-col cols='12' md="6">
                <v-text-field outlined dense placeholder="House Number" hide-details="auto"></v-text-field>
            </v-col>
            <v-col cols='12' md="6">
                <v-text-field outlined dense placeholder="Village" hide-details="auto"></v-text-field>
            </v-col>
            <v-col cols='12' md="6">
                <v-text-field outlined dense placeholder="District" hide-details="auto"></v-text-field>
            </v-col>
            <v-col cols='12' md="6">
                <v-text-field outlined dense placeholder="Province" hide-details="auto"></v-text-field>
            </v-col>
            <v-col cols='12' md="6">
                <v-text-field outlined dense placeholder="Active Status" hide-details="auto"></v-text-field>
            </v-col>
            <v-col cols='12'>
                <v-textarea outlined dense placeholder="Detail" hide-details="auto" counter="250"></v-textarea>
            </v-col>
            <v-card-actions>
                <v-btn color="red" dark width="150">Cancel</v-btn>
                <v-btn color="primary" width="150" >Save</v-btn>
            </v-card-actions>
    </v-row>
   </v-card>
  </v-container>
</template>

<script>
export default {

}
</script>
