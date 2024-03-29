<template>
  <v-app light>
    <section>
      <v-parallax
        src="./landing.jpeg"
        alt="Bathroom Landing Header Image"
        height="780"
      >
        <v-row align="center">
          <v-col
            cols="12"
            sm="8"
            md="8"
            lg="8"
            xl="8"
            class="text-center pb-0 pb-sm-16 pb-md-16 pb-lg-16 pb-xl-16"
          >
            <h1 class="headline text-h2 pb-4 black--text font-weight-bold">
              Septic System Inspections
            </h1>
            <h2 class="text-h4 font-weight-bold subheading green--text">
              Serving All of New Jersey
            </h2>
          </v-col>
          <!-- Contact Form -->
          <v-col
            v-if="!$vuetify.breakpoint.mobile"
            cols="12"
            sm="4"
            md="4"
            lg="4"
            xl="4"
            class="pa-0 pa-sm-16 pa-md-16 pa-lg-16 pa-xl-16"
          >
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
                  @click.prevent="submit(name, email, phone)"
                >
                  submit
                </v-btn>
                <v-alert v-if="successAlert" class="mt-5" type="success">
                  Thanks for filling out our form!
                </v-alert>
                <v-alert v-if="errorAlert" class="mt-5" type="error">
                  Please fix the errors above before submitting!
                </v-alert>
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

    <section class="px-0 px-sm-16 px-md-16 px-lg-16 px-xl-16">
      <v-row>
        <v-col
          class="text-h4 green--text pt-0"
          align="center"
          cols="12"
          sm="12"
          md="12"
          lg="12"
          xl="12"
        >
          Looking for a Septic Inspector?
        </v-col>
        <v-col cols="12" sm="6" md="6" lg="6" xl="6">
          <v-card
            class="elevation-0 transparent px-10 px-sm-16 px-md-16 px-lg-16 px-xl-16"
          >
            <v-card-text
              class="text-body-1 black--text pa-0 pa-sm-16 pa-md-16 pa-lg-16 pa-xl-16"
            >
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
        <v-col cols="12" sm="6" md="6" lg="6" xl="6">
          <v-card
            class="elevation-0 transparent pb-10 px-10 px-sm-16 px-md-16 px-lg-16 px-xl-16"
          >
            <v-card-text
              class="text-body-1 black--text pa-0 pa-sm-16 pa-md-16 pa-lg-16 pa-xl-16"
            >
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
    <section class="px-5 px-sm-16 px-md-16 px-lg-16 px-xl-16 pb-16 green">
      <v-row class="px-5 px-sm-16 px-md-16 px-lg-16 px-xl-16 pb-10">
        <v-col
          class="text-h4 white--text py-16"
          align="center"
          cols="12"
          sm="12"
          md="12"
          lg="12"
          xl="12"
        >
          Our Customers
        </v-col>
        <v-col cols="12" sm="4" md="4" lg="4" xl="4">
          <v-card class="mx-0 mx-sm-5 mx-md-5 mx-lg-5 mx-xl-5 text-center">
            <v-img
              class="white--text align-end"
              src="./HomeownersCard.png"
              alt="House"
            />
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
              An onsite wastewater treatment and disposal system, or Septic
              System, may be the most expensive component of your home. For home
              sellers, a pre-listing inspection can ensure that there are no
              surprises once the home is put on the market.
            </v-card-text>
          </v-card>
        </v-col>
        <v-col cols="12" sm="4" md="4" lg="4" xl="4">
          <v-card class="mx-0 mx-sm-5 mx-md-5 mx-lg-5 mx-xl-5 text-center">
            <v-img
              class="white--text align-end pb-10"
              src="./middleCard.webp"
              alt="House"
            />
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
              Buying a home is one of the biggest investments you will make, so
              you want to avoid any surprises after you purchase the home.
             
              For new prospective buyers and/or investors, inspection results can help you decide if the home is right for you.
            </v-card-text>
          </v-card>
        </v-col>
        <v-col cols="12" sm="4" md="4" lg="4" xl="4">
          <v-card class="mx-0 mx-sm-5 mx-md-5 mx-lg-5 mx-xl-5 text-center">
            <v-img
              class="white--text align-end"
              src="./ContactCard.png"
              alt="House"
            />
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

    <section class="px-5 px-sm-16 px-md-16 px-lg-16 px-xl-16 pb-16">
      <v-row class="px-5 px-sm-16 px-md-16 px-lg-16 px-xl-16 pb-16">
        <v-col class="text-h4 green--text pt-16" align="center" cols="12">
          Areas Served
        </v-col>
        <v-col cols="12" sm="6" md="6" lg="6" xl="6">
          <v-card
            class="elevation-0 transparent px-0 px-sm-16 px-md-16 px-lg-16 px-xl-16 pb-16"
          >
            <v-card-text class="text-h5 green--text text-center pa-16">
              Atlantic, Bergen, Burlington, Camden, Cape May, Cumberland, Essex,
              Gloucester, Hudson, Hunterdon, Mercer, Middlesex, Monmouth,
              Morris, Ocean, Passaic, Salem, Somerset, Sussex, Union, & Warren
              Counties
            </v-card-text>
            <v-divider class="mb-10" />
            <v-card-text class="black--text text-center text-body-1">
              With over 5 years of experience in residential septic system
              inspection, Murphy's Septic Inspection goes above and beyond to
              make your residential inspection quick and easy. Our friendly and
              knowledgable inspectors follow the reporting standards of the NJ
              DEP. We are happy to offer accurate and unbiased recommendations
              on advanced services and have access to a network of industry
              professionals who can help prolong your system's life. Schedule
              your free consultation today with one of our friendly inspectors.
            </v-card-text>
          </v-card>
        </v-col>
        <v-col align="center" cols="12" sm="6" md="6" lg="6" xl="6">
          <v-card
            class="elevation-0 transparent px-0 px-sm-16 px-md-16 px-lg-16 px-xl-16"
          >
            <v-card-text
              class="text-body-1 black--text pa-0 pa-sm-16 pa-md-16 pa-lg-16 pa-xl-16"
            >
              <v-img
                width="50%"
                src="./NewJerseyCounties.png"
                alt="New Jersey"
              />
            </v-card-text>
          </v-card>
        </v-col>
      </v-row>
    </section>

    <section
      class="px-0 px-sm-16 px-md-16 px-lg-16 px-xl-16 pb-16 green pt-10 white--text"
    >
      <v-row>
        <v-col class="text-h4" align="center" cols="12">
          Need a Home Septic Inspection? <br />
          Murphy's Can Be There!
        </v-col>
        <v-col cols="12" sm="6" md="6" lg="6" xl="6">
          <v-card
            class="elevation-0 transparent px-10 px-sm-16 px-md-16 px-lg-16 px-xl-16 pb-16"
          >
            <v-card-text
              class="text-body-1 white--text pa-0 pa-sm-16 pa-md-16 pa-lg-16 pa-xl-16"
            >
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
        <v-col cols="12" sm="6" md="6" lg="6" xl="6">
          <v-card
            class="elevation-0 transparent px-10 px-sm-16 px-md-16 px-lg-16 px-xl-16"
          >
            <v-card-text
              class="text-body-1 white--text pa-0 pa-sm-16 pa-md-16 pa-lg-16 pa-xl-16"
            >
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
    successAlert: false,
    errorAlert: false,
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
    async submit(name, email, phone) {
      this.$v.$touch()
      try {
        if (!this.$v.$error) {
          this.errorAlert = false
          this.$fire.database
            .ref('users')
            .push()
            .set({
              name: name,
              email: email,
              phone: phone,
            })
            .then((this.successAlert = true))
            .finally(
              setTimeout(() => {
                this.successAlert = false
              }, 5000)
            )
        } else {
          // handle error case
          this.errorAlert = true
        }
      } catch (err) {
        // handle errors
      }
    },
  },
}
</script>
