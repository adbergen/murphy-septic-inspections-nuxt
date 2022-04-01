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
          <v-btn v-for="icon in icons" :key="icon" icon color="black">
            <v-icon size="24px">
              {{ icon }}
            </v-icon>
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
    
    <v-footer color="grey" class="grey darken-4 white--text" height="395">
      <v-row>
        <v-col
          class="d-flex justify-center align-center"
          align="center"
          cols="4"
        >
          <v-tabs
            dark
            background-color="grey darken-4"
            class=""
            color="green"
            hide-slider
            v-model="tab"
            vertical
          >
            <v-tab to="/">Home</v-tab>
            <v-tab to="/about">About</v-tab>
            <v-tab to="/services">Services</v-tab>
            <v-tab to="/contact">Contact</v-tab>
          </v-tabs>
        </v-col>
        <v-col cols="4" align="center" class="pt-7">
          <v-card flat color="grey darken-4">
            <v-img src="./footerLogo.png" height="135px" width="260px" />
            <v-btn
              to="/contact"
              color="white"
              class="mt-7"
              rounded
              outlined
              label="yes"
              >Book a Consultation</v-btn
            >
          </v-card>
        </v-col>
        <v-col
          class="d-flex justify-center align-center"
          align="center"
          cols="4"
        >
          <v-card flat color="grey darken-4">
            <v-list color="grey darken-4" dark two-line>
              <v-list-item>
                <v-list-item-icon>
                  <v-icon color="green"> mdi-phone </v-icon>
                </v-list-item-icon>

                <v-list-item-content>
                  <v-list-item-title>(555) 555-5555</v-list-item-title>
                  <v-list-item-subtitle>Phone</v-list-item-subtitle>
                </v-list-item-content>
              </v-list-item>

              <v-divider inset></v-divider>

              <v-list-item>
                <v-list-item-icon>
                  <v-icon color="green"> mdi-email </v-icon>
                </v-list-item-icon>

                <v-list-item-content>
                  <v-list-item-title>info@murphysepticinspections.com</v-list-item-title>
                  <v-list-item-subtitle>Email</v-list-item-subtitle>
                </v-list-item-content>
              </v-list-item>

              <v-divider inset></v-divider>

              <v-list-item>
                <v-list-item-icon>
                  <v-icon color="green"> mdi-map-marker </v-icon>
                </v-list-item-icon>

                <v-list-item-content>
                  <v-list-item-title>1400 Main Street</v-list-item-title>
                  <v-list-item-subtitle>Jackson, NJ 08527</v-list-item-subtitle>
                </v-list-item-content>
              </v-list-item>
            </v-list>
          </v-card>
        </v-col>
        <v-col cols="12" class="text-center text-body-1"
          ><v-card dark flat color="grey darken-4"
            ><span>
              <v-card-text>
                <v-btn
                  v-for="icon in icons"
                  :key="icon"
                  class="mx-4 white--text"
                  icon
                >
                  <v-icon size="35px">
                    {{ icon }}
                  </v-icon>
                </v-btn>
              </v-card-text>
              &copy; Murphy Septic Inspections LLC
              {{ new Date().getFullYear() }}</span
            ></v-card
          ></v-col
        >
      </v-row>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  name: 'DefaultLayout',
  data() {
    return {
      tab: 'null',
      icons: ['mdi-facebook', 'mdi-linkedin', 'mdi-instagram'],
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
