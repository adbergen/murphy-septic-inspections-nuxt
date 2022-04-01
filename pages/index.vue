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

                <v-btn dark block color="green" class="mr-4 mt-2" @click="submit"> submit </v-btn>
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

    <section>
      <v-parallax height="380">
        <v-layout column align-center justify-center>
          <div class="headline white--text mb-3 text-xs-center">
            Endorfine is a social network that allows everyone to reach a huge
            audience with a tap
          </div>
          <em
            >With the power of Endorfine you don't need to be famous or post
            pics of cute cats in order to get visibility</em
          >
          <v-btn class="blue lighten-2 mt-5" large href="/pre-made-themes">
            Get more info
          </v-btn>
        </v-layout>
      </v-parallax>
    </section>

    <!-- Three Card Section -->
    <section>
      <v-layout column wrap class="my-3" align-center>
        <v-row>
          <div class="text-xs-center">
            <div class="headline text-h3">Looking for a Septic Inspector?</div>
          </div>
        </v-row>
        <v-flex xs12>
          <v-container grid-list-xl>
            <v-layout row wrap align-center>
              <v-flex xs12 md4>
                <v-card class="elevation-0 transparent">
                  <v-img
                    class="white--text align-end"
                    height="200px"
                    src="https://cdn.vuetifyjs.com/images/cards/docks.jpg"
                  >
                  </v-img>
                  <v-card-text class="text-xs-center">
                    <v-icon x-large class="blue--text text--lighten-2"
                      >public</v-icon
                    >
                  </v-card-text>
                  <v-card-title primary-title class="layout justify-center">
                    <div class="headline text-xs-center">Reach the world</div>
                  </v-card-title>
                  <v-card-text>
                    Show your stuff to the whole community of Endorfine not only
                    to your mum or your friends. We love making good content
                    viral. In this moment Endorfine is used by artists who are
                    not famous but that want to share their works to the world.
                    Unfortunately with other social networks this is hard, slow
                    and sometime expensive.
                  </v-card-text>
                </v-card>
              </v-flex>
              <v-flex xs12 md4>
                <v-card class="elevation-0 transparent">
                  <v-card-text class="text-xs-center">
                    <v-icon x-large class="blue--text text--lighten-2"
                      >flash_on</v-icon
                    >
                  </v-card-text>
                  <v-card-title primary-title class="layout justify-center">
                    <div class="headline">Fast feedback</div>
                  </v-card-title>
                  <v-card-text>
                    Time is important, we don't want you to waste it. Here you
                    can get a massive feedback from real users in minutes. And
                    if your stuff is appreciated you won't only get positive
                    feedback but also lovely and sincere fans
                  </v-card-text>
                </v-card>
              </v-flex>
              <v-flex xs12 md4>
                <v-card class="elevation-0 transparent">
                  <v-card-text class="text-xs-center">
                    <v-icon x-large class="blue--text text--lighten-2"
                      >share</v-icon
                    >
                  </v-card-text>
                  <v-card-title primary-title class="layout justify-center">
                    <div class="headline text-xs-center">
                      Create new connections
                    </div>
                  </v-card-title>
                  <v-card-text>
                    Imagine if you can directly speak with the world's
                    population. Don't you think it would be easier to find nice
                    people to interact with? Endorfine is both local and global
                    and help you to connect without limitations with people from
                    your city, your state and your universe!
                  </v-card-text>
                </v-card>
              </v-flex>
            </v-layout>
          </v-container>
        </v-flex>
      </v-layout>
    </section>

    <section>
      <v-container grid-list-md>
        <v-layout row wrap>
          <v-flex xs12 text-xs-center class="mt-5">
            <div class="headline">Are you amazed? Stay tuned!</div>
            <br />
            <div>
              We are lunching the beta in a few time. If you want to be one of
              the first Endorfine users we will email you as soon as we're
              ready. In the beginning only few people will test before the
              launch. Let us know how Endorfine will help you!
            </div>
          </v-flex>
          <v-flex xs8 offset-xs2> </v-flex>
        </v-layout>
      </v-container>
    </section>

    <section>
      <v-parallax height="380">
        <v-layout column align-center justify-center>
          <div class="headline white--text mb-3 text-xs-center">
            We are dropping cool news and opportunities on socials
          </div>
        </v-layout>
        <v-layout justify-space-around justify-center>
          <v-icon x-large dark>fab fa-facebook-f</v-icon>

          <v-icon x-large dark>fab fa-twitter</v-icon>

          <v-icon x-large dark>fab fa-reddit-alien</v-icon>

          <v-icon x-large dark>fab fa-instagram</v-icon>

          <v-icon x-large dark>fab fa-discord</v-icon>
        </v-layout>
      </v-parallax>
    </section>

    <section>
      <v-container grid-list-xl>
        <v-layout row wrap justify-center class="my-5">
          <v-flex xs12 sm4>
            <v-card class="elevation-0 transparent">
              <v-card-title primary-title class="layout justify-center">
                <div class="headline">Company info</div>
              </v-card-title>
              <v-card-text>
                We are not a company. We hate companies. Just imagine us like
                the guys from the Silicon Valley series.
              </v-card-text>
            </v-card>
          </v-flex>
          <v-flex xs12 sm4 offset-sm1>
            <v-card class="elevation-0 transparent">
              <v-card-title primary-title class="layout justify-center">
                <div class="headline">We are hiring</div>
              </v-card-title>
              <v-card-text>
                Are you a creative person? Do you like techy stuff? Complete the
                email form by writing your skills and interests
              </v-card-text>
            </v-card>
          </v-flex>
        </v-layout>
      </v-container>
    </section>

    <section>
      <v-container>
        <v-layout>
          <v-flex xs12 class="text-xs-center">
            <img height="200px" />
          </v-flex>
        </v-layout>
      </v-container>
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
