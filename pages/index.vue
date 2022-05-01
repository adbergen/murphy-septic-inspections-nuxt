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
        <v-col class="text-h4 green--text pt-0" align="center" cols="12">
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
              conditions.
            </v-card-text>
          </v-card>
        </v-col>
        <v-col cols="6">
          <v-card class="elevation-0 transparent px-16">
            <v-card-text class="text-body-1 black--text pa-16">
              Some local municipalities and New Jersey state regulations require
              a professional residential septic system inspection before
              completion. Murphy's certified and licensed inspectors will
              inspect your residential septic system thoroughly and make the
              process quick and painless.
              <br />
              <br />
              Our inspections typically take about 2 hours though it is
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
    <section class="px-16 pb-16 green">
      <v-row class="px-16 pb-10">
        <v-col class="text-h4 white--text py-16" align="center" cols="12">
          Who We Are
        </v-col>
        <v-col cols="4">
          <v-card class="mx-5 text-center">
            <v-img class="white--text align-end" src="./HomeownersCard.png" />
            <v-card-text
              style="transform: translateY(-50%)"
              class="text-center pb-0"
            >
              <v-avatar size="60px" color="green">
                <v-icon size="30px" dark> mdi-information </v-icon>
              </v-avatar>
            </v-card-text>
            <v-card-title class="justify-center text-h5 pt-0 pb-10">
              Homeowners/Sellers
            </v-card-title>
            <v-card-text class="black--text text-body-1">
              Complete septic system inspections are done for several reasons.
              We have an unparalleled commitment to excellence while providing
              quality service to a wide array of customers that include the
              residential, commercial and industrial sectors.
            </v-card-text>
          </v-card>
        </v-col>
        <v-col cols="4">
          <v-card class="mx-5 text-center">
            <v-img class="white--text align-end" src="./middleCard.webp" />
            <v-card-text
              style="transform: translateY(-50%)"
              class="text-center pb-0"
            >
              <v-avatar size="60px" color="green">
                <v-icon size="30px" dark> mdi-hammer-screwdriver </v-icon>
              </v-avatar>
            </v-card-text>
            <v-card-title class="justify-center text-h5 pt-0 pb-10">
              Buyers
            </v-card-title>
            <v-card-text class="black--text text-body-1">
              An onsite wastewater treatment and disposal system, or Septic
              System, may be the most expensive component of your home. For home
              sellers, a pre-listing inspection can ensure that there are no
              surprises once the home is put on the market.
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
              <v-avatar size="60px" color="green">
                <v-icon size="30px" dark> mdi-phone </v-icon>
              </v-avatar>
            </v-card-text>
            <v-card-title class="justify-center text-h5 pt-0 pb-10">
              No Conflict of Interest
            </v-card-title>
            <v-card-text class="black--text text-body-1">
              Feel confident choosing Murphy's Septic Inspections. Buying or
              selling, we do not offer any type of septic repair work so you do
              not have to worry about Murphy's finding problems that don't
              exist. Don't hesitate to reach out to us regarding any questions
              or concerns.
            </v-card-text>
          </v-card>
        </v-col>
      </v-row>
    </section>

    <section class="px-16">
      <v-row class="px-16">
        <v-col class="text-h4 green--text pt-16" align="center" cols="12">
          Areas Served
        </v-col>
        <v-col cols="6">
          <v-card class="elevation-0 transparent px-16">
            <v-card-text class="text-h5 green--text text-center pa-16">
              Atlantic, Bergen, Burlington, Camden, Cape May, Cumberland, Essex,
              Gloucester, Hudson, Hunterdon, Mercer, Middlesex, Monmouth,
              Morris, Ocean, Passaic, Salem, Somerset, Sussex, Union, & Warren
              Counties
            </v-card-text>
            <v-divider class="mb-10" inset />
            <v-card-text class="black--text text-center text-body-1">
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
        <v-col align="center" cols="6">
          <v-card class="elevation-0 transparent px-16">
            <v-card-text class="text-body-1 black--text pa-16">
              <v-img width="50%" src="./NewJerseyCounties.png" />
            </v-card-text>
          </v-card>
        </v-col>
      </v-row>
    </section>

    <section class="px-16 green pt-10 white--text">
      <v-row>
        <v-col class="text-h4" align="center" cols="12">
          Need a Home Septic Inspection? <br />
          Murphy's Can Be There!
        </v-col>
        <v-col cols="6">
          <v-card class="elevation-0 transparent px-16">
            <v-card-text class="text-body-1 white--text pa-16">
              Murphy Septic Inspection, LLC is a member of the National
              Association of Wastewater Technicians or NAWT. All of our septic
              inspections are performed in strict conformance to the NAWT’s
              Inspection Standards by certified NAWT inspectors. Due to these
              high standards, these specifications have been described by many
              as the Industry Standard for an on-lot residential septic system
              inspection in New Jersey and around the nation.
            </v-card-text>
          </v-card>
        </v-col>
        <v-col cols="6">
          <v-card class="elevation-0 transparent px-16">
            <v-card-text class="text-body-1 white--text pa-16">
              A comprehensive septic inspection provides you with valuable
              information about the present condition of the system, however, it
              is important to note that it is not a warranty that guarantees
              that the system will function properly for any period in the
              future. All of our expert residential septic system inspectors are
              highly trained and certified to inspect, identify problems and
              provide solutions. Reach out to see why Murphy is the right
              choice.
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

</style>
