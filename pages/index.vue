<template>
  <v-app light>
    <section>
      <v-parallax src="./LandingBackground.png" height="780">
        <v-row align="center">
          <v-col cols="8" class="text-center pb-16">
            <h2 class="headline text-h2 pb-4 black--text font-weight-bold">
              Septic System Inspections
            </h2>
            <span class="text-h4 font-weight-bold subheading green--text">
              Serving All of New Jersey
            </span>
          </v-col>
          <!-- Contact Form -->
          <v-col cols="4" class="pa-16">
            <v-card class="pb-10 pt-4 px-5">
              <v-card-title class="green--text font-weight-bold text-h5 pb-8"
                >Request a callback</v-card-title
              >
              <form class="px-12">
                <v-text-field
                  v-model="name"
                  :error-messages="nameErrors"
                  label="Name"
                  required
                  @input="$v.name.$touch()"
                  @blur="$v.name.$touch()"
                ></v-text-field>
                <v-text-field
                  v-model="email"
                  :error-messages="emailErrors"
                  label="E-mail"
                  required
                  @input="$v.email.$touch()"
                  @blur="$v.email.$touch()"
                ></v-text-field>
                <v-text-field
                  v-model="phone"
                  :error-messages="phoneErrors"
                  label="Phone Number"
                  required
                  @input="$v.phone.$touch()"
                  @blur="$v.phone.$touch()"
                ></v-text-field>

                <v-btn
                  dark
                  block
                  color="green"
                  class="mr-4 mt-2"
                  @click="submit"
                >
                  submit
                </v-btn>
              </form>
              <div class="text-center pt-4 text-body-1 px-10">
                Our team will be in touch as soon as possible to discuss your
                needs.
              </div>
            </v-card>
          </v-col>
        </v-row>
      </v-parallax>
    </section>

    <section class="px-16">
      <v-row>
        <v-col class="text-h4 green--text" align="center" cols="12">
          Looking for a Septic Inspector?
        </v-col>
        <v-col cols="6">
          <v-card class="elevation-0 transparent px-16">
            <v-card-text class="text-body-1 black--text pa-16">
              We perform residential septic system inspections for current
              homeowners and prospective real estate purchasers. An onsite
              wastewater treatment and disposal system, or what is more commonly
              referred to as a Septic System, may be the most expensive single
              component of your home. Therefore, if you want to save yourself
              some trouble in the future it's crucial that you know its
              condition and routinely have it checked. <br /><br />

              Getting a septic inspection provides you with information about
              the septic system components and their current operating
              conditions. Local municipalities and New Jersey state regulations
              require a professional residen-
            </v-card-text>
          </v-card>
        </v-col>
        <v-col cols="6">
          <v-card class="elevation-0 transparent px-16">
            <v-card-text class="text-body-1 black--text pa-16">
              tial septic system inspection before completion. Murphy's
              certified and licensed inspectors will inspect your residential
              septic system thoroughly and make the process quick and painless.
              <br />
              <br />
              Our inspections typically take about 3 hours though it is
              important to note every system is different and finding the
              components, exposing them, and dealing with any issues that may
              arise can take varied amounts of time. Your residential septic
              inspection report can be ready within 24 hours. We do not perform
              repairs in an effort to prevent conflict of interest in that area.
            </v-card-text>
          </v-card>
        </v-col>
      </v-row>
    </section>

    <!-- Three Card Section -->
    <section class="pa-16 green">
      <v-row class="pa-16">
        <v-col cols="4">
          <v-card class="mx-5 text-center">
            <v-img class="white--text align-end" src="./HomeownersCard.png" />
            <v-card-text
              style="transform: translateY(-50%)"
              class="text-center pb-0"
            >
              <v-avatar color="green">
                <v-icon dark> mdi-information </v-icon>
              </v-avatar>
            </v-card-text>
            <v-card-title class="justify-center text-h5 pt-0 pb-10">
              About Murphy's
            </v-card-title>
            <v-card-text class="black--text text-body-1">
              Complete system inspections are done for several reasons and we
              perform residential septic system inspections for both current
              homeowners and prospective real estate purchasers.
            </v-card-text>
          </v-card>
        </v-col>
        <v-col cols="4">
          <v-card class="mx-5 text-center">
            <v-img class="white--text align-end" src="./AboutCard.png" />
            <v-card-text
              style="transform: translateY(-50%)"
              class="text-center pb-0"
            >
              <v-avatar color="green">
                <v-icon dark> mdi-home </v-icon>
              </v-avatar>
            </v-card-text>
            <v-card-title class="justify-center text-h5 pt-0 pb-10">
              Services
            </v-card-title>
            <v-card-text class="black--text text-body-1">
              An onsite wastewater treatment and disposal system, or Septic
              System, may be the most expensive single component of your home.
              For home sellers, a pre-listing inspection can ensure that there
              are no surprises once their home is put on the market.
            </v-card-text>
          </v-card>
        </v-col>
        <v-col cols="4">
          <v-card class="mx-5 text-center">
            <v-img class="white--text align-end" src="./ContactCard.png" />
            <v-card-text
              style="transform: translateY(-50%)"
              class="text-center pb-0"
            >
              <v-avatar color="green">
                <v-icon dark> mdi-phone </v-icon>
              </v-avatar>
            </v-card-text>
            <v-card-title class="justify-center text-h5 pt-0 pb-10">
              Contact
            </v-card-title>
            <v-card-text class="black--text text-body-1">
              Feel confident choosing Murphy's Septic Inspections. Buying or
              selling, we do not offer any type of septic repair work so you do
              not have to worry about Murphy's finding problems that don't
              exist.
            </v-card-text>
          </v-card>
        </v-col>
      </v-row>
    </section>

    <section class="px-16">
      <v-row>
        <v-col class="text-h4 green--text pt-16" align="center" cols="12">
          Areas Served
        </v-col>
        <v-col cols="6">
          <v-card class="elevation-0 transparent px-16">
            <v-card-text class="text-body-1 black--text pa-16">
              Atlantic, Bergen, Burlington, Camden, Cape May, Cumberland, Essex,
              Gloucester, Hudson, Hunterdon, Mercer, Middlesex, Monmouth,
              Morris, Ocean, Passaic, Salem, Somerset, Sussex, Union, & Warren
              Counties
            </v-card-text>
            <v-card-text>
              With over 5 years of experience in residential septic system
              inspection, Murphy's Septic Inspection goes above and beyond to
              make your residential inspection quick and easy. Our friendly and
              knowledgable inspectors follow the reporting standards of the NJ
              DEP. We are happy to offer recommendations on advanced services
              and have access to a network of industry professionals who can
              help prolong your system's life. Schedule your free consultation
              today with one of our friendly inspectors.
            </v-card-text>
          </v-card>
        </v-col>
        <v-col cols="6">
          <v-card class="elevation-0 transparent px-16">
            <v-card-text class="text-body-1 black--text pa-16">
              <v-img width="50%" src="./NewJerseyCounties.png" />
            </v-card-text>
          </v-card>
        </v-col>
      </v-row>
    </section>
  </v-app>
</template>

<script>
import { validationMixin } from 'vuelidate'
import { required, email } from 'vuelidate/lib/validators'

export default {
  mixins: [validationMixin],

  validations: {
    name: { required },
    email: { required, email },
    phone: { required },
  },

  data: () => ({
    name: '',
    email: '',
    phone: '',
  }),

  computed: {
    nameErrors() {
      const errors = []
      if (!this.$v.name.$dirty) return errors
      !this.$v.name.required && errors.push('Name is required.')
      return errors
    },
    emailErrors() {
      const errors = []
      if (!this.$v.email.$dirty) return errors
      !this.$v.email.email && errors.push('Must be valid e-mail')
      !this.$v.email.required && errors.push('E-mail is required')
      return errors
    },
    phoneErrors() {
      const errors = []
      if (!this.$v.phone.$dirty) return errors
      !this.$v.phone.required && errors.push('Phone number is required')
      return errors
    },
  },

  methods: {
    submit() {
      this.$v.$touch()
    },
  },
}
</script>

<style scoped>
.finedTitle {
  font-weight: 900;
  text-shadow: 2px 2px #000000;
}

.social-icon {
  font-size: 21px;
  color: white;
}
</style>
