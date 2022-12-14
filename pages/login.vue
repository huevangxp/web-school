<template>
  <v-container fluid>
    <v-card max-width="600" class="mx-auto" elevation="0">
      <v-card-title>Login Form</v-card-title>
      <v-card-text>
        <v-row>
          <v-col cols="12">
            <v-text-field
              outlined
              dense
              placeholder="Phone"
              type="number"
              hide-details="0"
              append-icon="mdi-phone"
            ></v-text-field>
          </v-col>
          <v-col cols="12">
            <v-text-field
              outlined
              dense
              placeholder="Password"
              hide-details="0"
              :type="!showPass ? 'password' : 'text'"
              :append-icon="!showPass ? 'mdi-eye-off' : 'mdi-eye'"
              @click:append="showPass = !showPass"
            ></v-text-field>
          </v-col>
        </v-row>
      </v-card-text>
      <v-card-text>
        <v-checkbox label="Remeber Password"></v-checkbox>
      </v-card-text>
      <v-card-text>
        <v-btn @click="dialog = true">resend password</v-btn>
      </v-card-text>
      <v-card-actions>
        <v-spacer />
        <v-btn color="red" dark width="100">Cancel</v-btn>
        <v-btn color="primary" width="100">Login</v-btn>
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
          </v-row>
        </v-card-text>
        <v-divider></v-divider>
        <v-card-actions>
          <v-btn text outlined>Resend OTP</v-btn>
          <v-spacer></v-spacer>
          <v-btn color="error" @click="dialog = false">Cancel</v-btn>
          <v-btn color="primary" :disabled="!isActive " @click="isActive = sendOTP">Send</v-btn>
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
      showPass:false,
      length: 6,
    }
    },
    computed: {
        isActive() {
      return this.otp.length === this.length
    },
    },
  methods: {
      sendOTP() {
        this.$router.push('/login')
    }
  },
}
</script>
