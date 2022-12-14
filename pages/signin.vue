<template>

    <v-container fluid class="mt-12" >
      <v-card class="mx-auto pa-10" max-width="500" elevation="0">
        <v-card-title class="text-h6 font-weight-regular justify-space-between">
          <span>{{ currentTitle }}</span>
          <v-avatar
            color="primary lighten-2"
            class="subheading white--text"
            size="24"
            :v-text="step">{{ step }}</v-avatar>
        </v-card-title>
        <v-window v-model="step">
          <v-window-item :value="1">
            <v-card-text>
              <v-text-field
                placeholder="User Name"
                outlined
                dense
              ></v-text-field>
              <v-text-field
                outlined
                dense
                placeholder="Position"
              ></v-text-field>
             
              <span class="text-caption grey--text text--darken-1">
                This is the email you will use to login to your Vuetify account
              </span>
            </v-card-text>
          </v-window-item>
          <v-window-item :value="2">
            <v-card-text>
                <v-text-field
                name="Phone"
                outlined
                dense
                placeholder="Phone"
              ></v-text-field>
              <v-text-field
                placeholder="Password"
                outlined
                dense
                :type="showPass ? 'text' : 'password'"
                :append-icon="showPass ? 'mdi-eye' : 'mdi-eye-off'"
                @click:append="showPass = !showPass"
              ></v-text-field>
            
              <span class="text-caption grey--text text--darken-1">
                Please enter a password for your account
              </span>
            </v-card-text>
          </v-window-item>
        </v-window>
        <v-divider></v-divider>
        <v-card-actions>
          <v-btn :disabled="step === 1" text @click="step--"> Back </v-btn>
          <v-spacer></v-spacer>
          <v-btn
            :disabled="step === 2"
            color="primary"
            depressed
            :class="step === 2 ? 'd-none' : ''"
            @click="step++">
            Next
          </v-btn>
          <v-btn
            color="primary"
            :class="step === 2 ? '' : 'd-none'"
            @click="login"
            >Register</v-btn
          >
        </v-card-actions>
      </v-card>
    </v-container>
</template>

<script>
export default {
  name: 'SignUpPage',
  data: () => ({
    step: 1,
    showPass: false,
  }),

  computed: {
    currentTitle() {
      switch (this.step) {
        case 1:
          return 'Sign In Information'
        case 2:
          return 'Sign In by password'
        default:
          return 'Choose Image'
      }
    },
  },
  methods: {
      login() {
        this.userData = true
   }
  },
}
</script>