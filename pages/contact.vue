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
              Contact
            </h2>
          </v-col>
        </v-row>
      </v-parallax>
    </section>

    <section>
      <v-row>
        <v-col
          cols="12"
          sm="4"
          md="4"
          lg="4"
          xl="4"
          class="pl-5 pl-sm-16 pl-md-16 pl-lg-16 pl-xl-16 pt-10 pt-sm-16 pt-md-16 pt-lg-16 pt-xl-16 pr-5"
        >
          <div class="pl-0 pl-sm-16 pl-md-16 pl-lg-16 pl-xl-16">
            <v-card class="px-10 px-sm-10 px-md-10 px-lg-10 px-xl-10">
              <v-card-title
                class="text-h4 green--text pt-5 pt-sm-10 pt-md-10 pt-lg-10 pt-xl-10"
              >
                <v-img
                  src="./HeaderLogo.png"
                  alt="Murphy Septic Inspections Logo"
                />
              </v-card-title>
              <v-list two-line>
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
          </div>
        </v-col>
        <v-col
          cols="12"
          sm="8"
          md="8"
          lg="8"
          xl="8"
          class="pa-5 pa-sm-16 pa-md-16 pa-lg-16 pa-xl-16"
        >
          <div class="px-0 px-sm-10 px-md-10 px-lg-10 px-xl-10">
            <v-card class="pb-10 pt-4 px-5">
              <v-card-title
                class="green--text font-weight-bold text-center justify-center text-h4 pb-8"
                style="word-break: break-word"
                >Send us a message</v-card-title
              >
              <form class="px-12">
                <v-text-field
                  v-model="name"
                  :error-messages="nameErrors"
                  label="Name"
                  outlined
                  required
                  @input="$v.name.$touch()"
                  @blur="$v.name.$touch()"
                ></v-text-field>
                <v-text-field
                  v-model="email"
                  :error-messages="emailErrors"
                  label="E-mail"
                  outlined
                  required
                  @input="$v.email.$touch()"
                  @blur="$v.email.$touch()"
                ></v-text-field>
                <v-text-field
                  v-model="phone"
                  :error-messages="phoneErrors"
                  label="Phone Number"
                  outlined
                  required
                  @input="$v.phone.$touch()"
                  @blur="$v.phone.$touch()"
                ></v-text-field>
                <v-textarea
                  v-model="message"
                  :error-messages="messageErrors"
                  outlined
                  label="Message"
                  required
                  @input="$v.message.$touch()"
                  @blur="$v.message.$touch()"
                ></v-textarea>
                <v-btn
                  dark
                  block
                  color="green"
                  class="mr-4 mt-2"
                  @click.prevent="submit(name, email, phone, message)"
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
          </div>
        </v-col>
      </v-row>
    </section>
  </div>
</template>

<script>
import { validationMixin } from 'vuelidate'
import { required, email } from 'vuelidate/lib/validators'

export default {
  name: 'contact',
  mixins: [validationMixin],
  validations: {
    name: { required },
    email: { required, email },
    phone: { required },
    message: { required },
  },

  data: () => ({
    name: '',
    email: '',
    phone: '',
    message: '',
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
    messageErrors() {
      const errors = []
      if (!this.$v.message.$dirty) return errors
      !this.$v.message.required && errors.push('Message is required')
      return errors
    },
  },

  async mounted() {
    // Initialize recaptcha instance
    try {
      await this.$recaptcha.init()
    } catch (e) {
      console.log(e)
    }
  },

  methods: {
    async submit(name, email, phone, message) {
      this.$v.$touch()
      try {
        // Start the verification process
        const response = await this.verifyCaptcha()

        // Display error message if verification was not successful
        if (!response.success || this.$v.$error) {
          this.$recaptcha.reset()
          this.errorAlert = true
          return
        }
        // Otherwise Submit form
        this.errorAlert = false
        this.$fire.database
          .ref('users')
          .push()
          .set({
            name: name,
            email: email,
            phone: phone,
            message: message,
          })
          .then((this.successAlert = true))
          .finally(
            setTimeout(() => {
              this.successAlert = false
            }, 5000)
          )
        this.$recaptcha.reset()
      } catch (error) {
        console.log(error)
      }
    },
    async verifyCaptcha() {
      try {
        const token = await this.$recaptcha.execute()
        const response = await this.$axios.$post(
          `/captcha-api/siteverify?secret=${process.env.SECRET_KEY}&response=${token}`
        )
        console.log(response)
        return response
      } catch (error) {
        return error
      }
    },
  },
}
</script>
