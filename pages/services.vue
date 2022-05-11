<template>
  <div light>
    <section>
      <v-parallax
        src="./GreenBanner.png"
        alt="Green Pipes Header Image"
        height="200"
      >
        <v-row align="center">
          <v-col cols="12" class="text-center">
            <h2
              class="headline text-h3 text-decoration-underline white--text font-weight-bold"
            >
              Services
            </h2>
          </v-col>
        </v-row>
      </v-parallax>
    </section>

    <!-- Three Card Section -->
    <section class="px-0 px-sm-16 px-md-16 px-lg-16 px-xl-16">
      <v-row class="py-16 pa-sm-16 pa-md-16 pa-lg-16 pa-xl-16">
        <v-col cols="12" sm="4" md="4" lg="4" xl="4">
          <v-card class="mx-5 text-center transparent elevation-0">
            <v-card-text
              style="transform: translateY(-50%)"
              class="text-center pb-0"
            >
              <v-icon color="green" size="50px"> mdi-lock </v-icon>
            </v-card-text>
            <v-card-title
              style="word-break: break-word"
              class="justify-center text-h5 green--text pt-0 pb-10"
            >
              Quick 24 Hour Reports
            </v-card-title>
            <v-card-text class="black--text text-h6 text-center">
              We value your time and know that Septic Inspections can be
              intimidating. Our expert inspectors guide you through the process
              and help you better understand your system.
            </v-card-text>
          </v-card>
          <v-divider class="mx-10" />
        </v-col>
        <v-col cols="12" sm="4" md="4" lg="4" xl="4">
          <v-card class="mx-5 text-center transparent elevation-0">
            <v-card-text
              style="transform: translateY(-50%)"
              class="text-center pb-0"
            >
              <v-icon color="green" size="50px"> mdi-clipboard </v-icon>
            </v-card-text>
            <v-card-title
              style="word-break: break-word"
              class="justify-center text-h5 green--text pt-0 pb-10"
            >
              NAWT Qualified & Licensed
            </v-card-title>
            <v-card-text class="black--text text-h6 text-center">
              Murphy’s Septic Inspections performs both residential and
              commercial septic system inspections for current homeowners and
              prospective real estate purchasers.
            </v-card-text>
          </v-card>
          <v-divider class="mx-10" />
        </v-col>
        <v-col cols="12" sm="4" md="4" lg="4" xl="4">
          <v-card class="mx-5 text-center transparent elevation-0">
            <v-card-text
              style="transform: translateY(-50%)"
              class="text-center pb-0"
            >
              <v-icon color="green" size="50px"> mdi-seal </v-icon>
            </v-card-text>
            <v-card-title
              style="word-break: break-word"
              class="justify-center text-h5 green--text pt-0 pb-10"
            >
              All Our Work Is Certified
            </v-card-title>
            <v-card-text class="black--text text-h6 text-center">
              Murphy’s certified and licensed inspectors will inspect your
              residential septic system thoroughly and make the process quick
              and painless.
            </v-card-text>
          </v-card>
          <v-divider class="mx-10" />
        </v-col>
      </v-row>
    </section>
  </div>
</template>

<script>
export default {
  name: 'services',
}
</script>
