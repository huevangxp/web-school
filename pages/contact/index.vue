<template>
  <v-container fluid>
    <v-card max-width="700" class="mx-auto pa-3">
      <v-card-title>TAMIXAY SCHOOL</v-card-title>
      <v-card-text
        >Lorem ipsum dolor sit, amet consectetur adipisicing elit. Repellat
        tenetur harum nesciunt alias aliquid sunt illum iure omnis adipisci
        doloremque perferendis consequuntur eos, explicabo fuga voluptatum ut
        ipsa. Voluptatum, ullam?</v-card-text
      >
      <v-row>
        <v-col cols="12 " md="6">
          <v-text-field outlined dense placeholder="Phone" hide-details="auto"></v-text-field>
        </v-col>
        <v-col cols="12 " md="6">
          <v-text-field outlined dense placeholder="Name or Title" hide-details="auto"></v-text-field>
        </v-col>
        <v-col cols="12">
          <v-textarea outlined counter="300"></v-textarea>
        </v-col>
      </v-row>
      <v-card-actions>
        <v-spacer></v-spacer>
        <v-btn color="primary" @click="dialog = true">
          send to school <v-icon class="ml-4">mdi-send</v-icon>
        </v-btn>
      </v-card-actions>
    </v-card>
    <v-dialog v-model="dialog" width="500" class="pa-6">
      <v-card class="pa-4">
        <v-card-title class="mb-3">
          Please Input OTP from message
        </v-card-title>
        <v-card-text>
          <v-row>
            <v-col cols="12">
              <div class="ma-auto" style="max-width: 300px">
                <v-otp-input v-model="otp" :length="length"></v-otp-input>
              </div>
            </v-col>

            <!-- <v-col cols="12" class="my-3">
            </v-col> -->
          </v-row>
        </v-card-text>
        <v-divider></v-divider>

        <v-card-actions>
            <v-btn text outlined>Resend OTP</v-btn>
          <v-spacer></v-spacer>
          <v-btn color="error" @click="dialog = false">Cancel</v-btn>
          <v-btn color="primary" :disabled="!isActive">Ready</v-btn>
        </v-card-actions>
      </v-card>
    </v-dialog>
  </v-container>
</template>

<script>
export default {
  data() {
    return {
      dialog: false,
      otp: '',
      length: 6,
    }
  },
  computed: {
    isActive() {
      return this.otp.length === this.length
    },
  },
}
</script>
