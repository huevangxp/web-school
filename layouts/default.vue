<template>
  <div>
    <v-app v-if="$vuetify.breakpoint.mobile" fixed app>
      <!-- <v-app-bar scroll-off-screen scroll-threshold> -->
      <v-main class="mb-16">
        <Nuxt />
      </v-main>
      <v-navigation-drawer v-model="drawer" right temporary  fixed app>
        <v-list-item active-class="deep-purple--text text--accent-4">
          <v-list-item-avatar>
            <v-img src="https://randomuser.me/api/portraits/men/78.jpg"></v-img>
          </v-list-item-avatar>

          <v-list-item-content>
            <v-list-item-title>John Leider</v-list-item-title>
          </v-list-item-content>
          <v-btn icon @click="drawer = false">
            <v-icon>mdi-window-close</v-icon>
          </v-btn>
        </v-list-item>

        <v-divider></v-divider>

        <v-list-item
          v-for="(item, i) in items"
          :key="i"
          :to="item.to"
          router
          exact
        >
          <v-list-item-action>
            <v-icon color="primary">{{ item.icon }}</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title>{{ item.title }}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-navigation-drawer>

      <v-app-bar fixed app elevation="0" scroll-off-screen color="primary" dark>
        <v-avatar size="50">
          <v-img
            src="data:image/jpeg;base64,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"
          ></v-img>
        </v-avatar>
        <v-card-title> TAMIXAY SCHOOL </v-card-title>
        <v-spacer />
        <v-btn  icon dark @click="drawer = !drawer">
          <v-icon> mdi-menu </v-icon>
        </v-btn>
      </v-app-bar>
      <v-footer padless tile shaped>
        <FooterPage />
      </v-footer>
    </v-app>

    <v-app v-else dark >
      <v-app-bar fixed app color="primary" dark>
        <v-avatar size="60">
          <v-img
            src="data:image/jpeg;base64,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"
          ></v-img>
        </v-avatar>
        <v-card-title> TAMIXAY SCHOOL </v-card-title>
        <v-spacer />
        <v-btn text dark to="/">Home</v-btn>
        <v-btn text dark to="/news">News</v-btn>
        <v-btn text dark to="/image">Gallery</v-btn>
        <v-btn text dark to="/contact">Contact Us</v-btn>
        <v-btn text dark to="/about">About</v-btn>
        <v-spacer />
        <v-menu v-if="userData" bottom left>
          <template  #activator="{ on, attrs}">
            <v-btn  dark icon v-bind="attrs" v-on="on">
              <v-icon>mdi-menu</v-icon>
            </v-btn>
          </template>
          <v-list>
            <v-list-item v-for="item  in user" :key="item.id" :to="item.to">
              <v-list-item-action>
                <v-icon color="primary">{{ item.icon }}</v-icon>
              </v-list-item-action>
              <v-list-item-title>{{ item.title }}</v-list-item-title>
            </v-list-item>
          </v-list>
          <v-list>
            <v-list-item @click="logout" >
              <v-list-item-action>
                <v-icon color="primary">mdi-power</v-icon>
              </v-list-item-action>
              <v-list-item-title>Logout</v-list-item-title>
            </v-list-item>
          </v-list>
          <!-- <v-btn text @click="logout"> <v-icon class="mr-7" color="primary">mdi-power</v-icon> Logout</v-btn> -->
        </v-menu>
        <v-btn v-else text dark  v-on="on" @click="login"> Login </v-btn>
      </v-app-bar>
      <v-main>
        <v-container fluid>
          <Nuxt />
        </v-container>
      </v-main>
      <v-footer padless tile shaped>
        <FooterPage />
      </v-footer>
    </v-app>
  </div>
</template>

<script>
export default {
  name: 'School',
  data() {
    return {
      userData: true,
      drawer: false,
      items: [
        {
          icon: 'mdi-home',
          title: 'Home',
          to: '/',
        },
        {
          icon: 'mdi-newspaper',
          title: 'News',
          to: '/news',
        },
        {
          icon: 'mdi-view-gallery-outline',
          title: 'Gallery',
          to: '/image',
        },
        {
          icon: 'mdi-account-box',
          title: 'Contact Us',
          to: '/contact',
        },
        {
          icon: 'mdi-information',
          title: 'About',
          to: '/about',
        },
      ],
      user: [
        {
          icon: 'mdi-account',
          title: 'Profile',
          to: '/profile',
        },
        {
          icon: 'mdi-account-multiple-plus',
          title: 'Add Student',
          to: '/profile/adduser',
        },
        {
          icon: 'mdi-human-male-board',
          title: 'Add Teacher',
           to: '/profile/addteacher',
        },
        {
          icon: 'mdi-message-check',
          title: 'Add Student absent',
           to: '/profile/absent',
        },

      ],

    }
  },
  methods: {
    logout() {
    this.userData = false
    },
    login() {
      this.userData = true
    }
  }
}
</script>
