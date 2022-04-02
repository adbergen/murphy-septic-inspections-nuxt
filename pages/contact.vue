<template>
  <div light>
    <section>
      <v-parallax src="./GreenBanner.png" height="200">
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
        <v-col cols="4" class="pl-16 pt-16">
          <div class="pl-16">
            <v-card class="px-10">
              <v-card-title class="text-h4 green--text pt-10">
                <v-img src="./HeaderLogo.png" />
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
                    <v-list-item-title>1400 Main Street</v-list-item-title>
                    <v-list-item-subtitle
                      >Jackson, NJ 08527</v-list-item-subtitle
                    >
                  </v-list-item-content>
                </v-list-item>
              </v-list>
            </v-card>
          </div>
        </v-col>
        <v-col cols="8" class="pa-16">
          <div class="px-16">
            <v-card class="pb-10 pt-4 px-5">
              <v-card-title
                class="green--text font-weight-bold text-center justify-center text-h4 pb-8"
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
                  name="input-7-4"
                  label="Message"
                  required
                  @input="$v.phone.$touch()"
                  @blur="$v.phone.$touch()"
                ></v-textarea>

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
    phoneErrors() {
      const errors = []
      if (!this.$v.message.$dirty) return errors
      !this.$v.message.required && errors.push('Message is required')
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
