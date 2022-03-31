<template>
  <v-app dark>
    <!-- <v-app-bar app height="90px">
      <NuxtLink to="/about">
        <v-img src="./headerLogo.png" width="300px" />
      </NuxtLink>

      <v-break />
      <v-tabs v-model="tab">
        <v-tab to="/">Home</v-tab>
        <v-tab to="/about">About</v-tab>
        <v-tab to="/services">Services</v-tab>
        <v-tab to="/contact">Contact</v-tab>
      </v-tabs>

      <v-btn icon @click.stop="rightDrawer = !rightDrawer">
        <v-icon>mdi-facebook</v-icon>
      </v-btn>
      <v-btn icon @click.stop="rightDrawer = !rightDrawer">
        <v-icon>mdi-instagram</v-icon>
      </v-btn>
      <v-btn icon @click.stop="rightDrawer = !rightDrawer">
        <v-icon>mdi-linkedin</v-icon>
      </v-btn>

      <v-btn icon @click.stop="rightDrawer = !rightDrawer">
        <v-icon>mdi-menu</v-icon>
      </v-btn>
    </v-app-bar> -->

    <!-- Navbar -->
    <v-app-bar color="white" height="80px" app>
      <v-row align="center" justify="center">
        <v-col cols="2" class="pa-none">
          <NuxtLink to="/about">
            <v-img src="./headerLogo.png" width="1000px" />
          </NuxtLink>
        </v-col>
        <v-col class="d-flex justify-space-around">
          <v-toolbar-title class="white--text"
            ><v-tabs color="green" v-model="tab">
              <v-tab to="/">Home</v-tab>
              <v-tab to="/about">About</v-tab>
              <v-tab to="/services">Services</v-tab>
              <v-tab to="/contact">Contact</v-tab>
            </v-tabs></v-toolbar-title
          >
        </v-col>
        <v-col cols="2" class="d-flex justify-end">
          <v-btn icon @click.stop="rightDrawer = !rightDrawer">
            <v-icon color="black">mdi-facebook</v-icon>
          </v-btn>
          <v-btn color="black" icon @click.stop="rightDrawer = !rightDrawer">
            <v-icon>mdi-instagram</v-icon>
          </v-btn>
          <v-btn color="black" icon @click.stop="rightDrawer = !rightDrawer">
            <v-icon>mdi-linkedin</v-icon>
          </v-btn>
        </v-col>
      </v-row>
    </v-app-bar>

    <!-- Nuxt Main View Container -->
    <v-main>
      <Nuxt />
    </v-main>

    <!-- Right Side Drawer -->
    <v-navigation-drawer v-model="rightDrawer" :right="right" temporary fixed>
      <v-list>
        <v-list-item @click.native="right = !right">
          <v-list-item-action>
            <v-icon light> mdi-repeat </v-icon>
          </v-list-item-action>
          <v-list-item-title>Switch drawer (click me)</v-list-item-title>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>

    <!-- Footer -->
    <v-footer class="grey darken-4 white--text"   height="395">
      <span>&copy; {{ new Date().getFullYear() }}</span>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  name: 'DefaultLayout',
  data() {
    return {
      tab: 'null',
      clipped: false,
      drawer: false,
      fixed: false,
      items: [
        {
          icon: 'mdi-apps',
          title: 'Welcome',
          to: '/',
        },
        {
          icon: 'mdi-chart-bubble',
          title: 'Inspire',
          to: '/inspire',
        },
      ],
      miniVariant: false,
      right: true,
      rightDrawer: false,
      title: 'Vuetify.js',
    }
  },
}
</script>
