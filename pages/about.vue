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
              About
            </h2>
          </v-col>
        </v-row>
      </v-parallax>
    </section>

    <section>
      <v-row align="center" justify="center">
        <v-col cols="12" sm="12" md="12" lg="6" xl="6">
          <v-img
            class="ma-16"
            src="./aboutImage.webp"
            alt="Septic Inspection Overview"
          />
        </v-col>
        <v-col cols="12" sm="12" md="12" lg="6" xl="6">
          <v-card class="elevation-0 transparent px-16 pb-16">
            <v-card-title
              class="text-h4 green--text"
              style="word-break: break-word"
            >
              Meet your Septic Inspector
            </v-card-title>
            <v-card-text class="text-body-1 black--text">
              As an independent septic inspection company, Murphy's Septic
              Inspection LLC is certified in full-service, on-site wastewater
              system inspections for new real estate buyers and current
              homeowners. We proudly serve residential clients in all of New
              Jersey and swear by our green technology which utilizes
              state-of-the-art equipment and environmentally friendly products
              to get your job done.
              <br /><br />
              Current residential septic system requirements in New Jersey can
              vary by the municipality which can quickly become confusing and
              overwhelming. That's why new homeowners can rely on Murphy's to
              get the job done without hassle. We have inspected over 5,000
              homes and our primary duty is to educate you regarding the prop er
              use and maintenance of your septic system.
              <br /><br />
              With experience and knowledge about the unique inspection
              requirements for your local area, our highly trained inspectors
              can complete a thorough investigation in just a few short hours.
              We then provide you with a detailed inspection report and handle
              all the local reporting paperwork on your behalf, making the
              process as simple as can be.
            </v-card-text>
          </v-card>
        </v-col>
      </v-row>
    </section>
  </div>
</template>

<script>
export default {
  name: 'about',
}
</script>
