<template>
  <v-app dark>
    <!-- Navbar -->
    <v-app-bar
      color="white"
      height="80px"
      app
      v-if="!$vuetify.breakpoint.mobile"
    >
      <v-row align="center" justify="center">
        <v-col cols="2" class="pa-none">
          <NuxtLink to="/">
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
        <!-- Social Links -->
        <v-col cols="2" class="d-flex justify-end">
          <v-btn
            lg
            v-for="icon in icons"
            :key="icon"
            icon
            color="grey darken-4"
          >
            <v-icon size="30px">
              {{ icon }}
            </v-icon>
          </v-btn>
        </v-col>
      </v-row>
    </v-app-bar>

    <!-- Mobile Nav -->
    <v-app-bar v-else color="white" height="80px" app>
      <NuxtLink to="/">
        <v-img src="./headerLogo.png" width="200px" />
      </NuxtLink>
      <v-spacer />
      <v-btn icon @click.stop="rightDrawer = !rightDrawer">
        <v-icon>mdi-menu</v-icon>
      </v-btn>
    </v-app-bar>

    <!-- Nuxt Main View Container -->
    <v-main>
      <Nuxt />
    </v-main>

    <!-- Right Side Drawer -->
    <v-navigation-drawer
      width="300px"
      v-model="rightDrawer"
      :right="right"
      temporary
      fixed
    >
      <v-list nav dense>
        <v-list-item-group
          align="center"
          v-model="navDrawer"
          active-class="green--text text--green"
        >
          <NuxtLink to="/">
            <v-list-item>
              <v-list-item-title>Home</v-list-item-title>
            </v-list-item>
          </NuxtLink>

          <NuxtLink to="/about">
            <v-list-item>
              <v-list-item-title>About</v-list-item-title>
            </v-list-item>
          </NuxtLink>

          <NuxtLink to="/services">
            <v-list-item>
              <v-list-item-title>Services</v-list-item-title>
            </v-list-item>
          </NuxtLink>

          <NuxtLink to="/contact">
            <v-list-item>
              <v-list-item-title>Contact</v-list-item-title>
            </v-list-item>
          </NuxtLink>
        </v-list-item-group>

        <div style="position: absolute; bottom: 0">
          <v-divider></v-divider>
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
              <v-list-item-title
                >info@murphysepticinspections.com</v-list-item-title
              >
              <v-list-item-subtitle>Email</v-list-item-subtitle>
            </v-list-item-content>
          </v-list-item>

          <v-divider inset></v-divider>

          <v-list-item>
            <v-list-item-icon>
              <v-icon color="green"> mdi-map-marker </v-icon>
            </v-list-item-icon>

            <v-list-item-content>
              <v-list-item-title>PO BOX 827</v-list-item-title>
              <v-list-item-subtitle>Ocean Gate, NJ 08740</v-list-item-subtitle>
            </v-list-item-content>
          </v-list-item>
        </div>
      </v-list>
    </v-navigation-drawer>

    <!-- Footer -->
    <v-footer color="grey" class="grey darken-4 white--text" height="395">
      <v-row>
        <v-col
          v-if="!$vuetify.breakpoint.mobile"
          class="d-flex justify-center align-center"
          align="center"
          cols="4"
          sm="4"
          md="4"
          lg="4"
          xl="4"
        >
          <!-- Footer Tabs -->
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
        <v-col
          cols="12"
          sm="4"
          md="4"
          lg="4"
          xl="4"
          align="center"
          class="pt-10"
        >
          <!-- Footer Logo -->
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
          v-if="!$vuetify.breakpoint.mobile"
          class="d-flex justify-center align-center pt-8"
          align="center"
          cols="4"
          sm="4"
          md="4"
          lg="4"
          xl="4"
        >
          <!-- Contact Details -->
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
                  <v-list-item-title
                    >info@murphysepticinspections.com</v-list-item-title
                  >
                  <v-list-item-subtitle>Email</v-list-item-subtitle>
                </v-list-item-content>
              </v-list-item>

              <v-divider inset></v-divider>

              <v-list-item>
                <v-list-item-icon>
                  <v-icon color="green"> mdi-map-marker </v-icon>
                </v-list-item-icon>

                <v-list-item-content>
                  <v-list-item-title>PO BOX 827</v-list-item-title>
                  <v-list-item-subtitle
                    >Ocean Gate, NJ 08740</v-list-item-subtitle
                  >
                </v-list-item-content>
              </v-list-item>
            </v-list>
          </v-card>
        </v-col>
        <v-col cols="12" class="text-center text-body-1"
          ><v-card dark flat color="grey darken-4"
            ><span>
              <!-- Social Links -->
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
      right: true,
      rightDrawer: false,
      navDrawer: 'Home',
    }
  },
}
</script>
