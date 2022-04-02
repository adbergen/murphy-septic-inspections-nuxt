<template>
  <div light>
    <section>
      <v-parallax src="./GreenBanner.png" height="200">
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
    <section class="px-16">
      <v-row class="px-16 pb-16">
        <v-col class="text-h4 white--text" align="center" cols="12">
          Who We Are
        </v-col>
        <v-col cols="4">
          <v-card class="mx-5 text-center transparent elevation-0">
            <v-card-text
              style="transform: translateY(-50%)"
              class="text-center pb-0"
            >
              <v-icon color="green" size="50px"> mdi-lock </v-icon>
            </v-card-text>
            <v-card-title class="justify-center text-h5 green--text pt-0 pb-10">
              Quick 24 Hour Reports
            </v-card-title>
            <v-card-text class="black--text text-h6 text-center">
              We value your time and know that Septic Inspections can be
              intimidating. Our expert inspectors guide you through the process
              and help you better understand your system.
            </v-card-text>
          </v-card>
        </v-col>
        <v-col cols="4">
          <v-card class="mx-5 text-center transparent elevation-0">
            <v-card-text
              style="transform: translateY(-50%)"
              class="text-center pb-0"
            >
              <v-icon color="green" size="50px"> mdi-clipboard </v-icon>
            </v-card-text>
            <v-card-title class="justify-center text-h5 green--text pt-0 pb-10">
              NAWT Qualified & Licensed
            </v-card-title>
            <v-card-text class="black--text text-h6 text-center">
              Murphy’s Septic Inspections performs both residential and
              commercial septic system inspections for current homeowners and
              prospective real estate purchasers.
            </v-card-text>
          </v-card>
        </v-col>
        <v-col cols="4">
          <v-card class="mx-5 text-center transparent elevation-0">
            <v-card-text
              style="transform: translateY(-50%)"
              class="text-center pb-0"
            >
              <v-icon color="green" size="50px"> mdi-seal </v-icon>
            </v-card-text>
            <v-card-title class="justify-center text-h5 green--text pt-0 pb-10">
              All Our Work Is Certified
            </v-card-title>
            <v-card-text class="black--text text-h6 text-center">
              Murphy’s certified and licensed inspectors will inspect your
              residential septic system thoroughly and make the process quick
              and painless.
            </v-card-text>
          </v-card>
        </v-col>
      </v-row>
    </section>

    <section class="px-16 grey lighten-4 pt-16">
      <v-row>
        <v-col class="text-h4 green--text pt-0" align="center" cols="12">
          Our Service
        </v-col>
        <v-col cols="6">
          <v-card class="elevation-0 transparent px-16">
            <v-card-text class="text-body-1 black--text px-16">
              Murphy's Septic Inspections pledges to be an industry leader in
              New Jersey and follow the reporting standards of the NJ DEP
              strictly. Typically, our wastewater treatment system inspections
              start by obtaining the septic system designs from your local
              authority. If an escavator or additional equipment is necessary,
              our partners can provide this service as at an additional cost.
              <br />
              <br />
              Depending on the type of inspection, some septics require
              extensive digging due to various components being very deep and
              difficult to find. The underground utilities must be marked out,
              whether digging is done with a machine. We will advise you ahead
              of time what to expect, ask you to fill out a maintenance history
              questionnaire, and confirm with you before arrival.
              <br />
              <br />
              If heavier machinery is needed, our inspectors are capable of
              handling it with the most precise movements, leaving as little of
              an impact as possible while also making sure the system is running
              as it should.
            </v-card-text>
          </v-card>
        </v-col>
        <v-col cols="6">
          <v-card class="elevation-0 transparent px-16 pb-16">
            <v-card-text class="text-body-1 black--text px-16">
              Our inspection crew is well-trained to handle all different types
              of septic systems and components of the system. The inspection
              process is usually quick but may take up to 2 hours to complete.
              <br />
              <br />
              We then open the septic tank, check the levels, and use an
              underground inline camera to inspect the connecting lines. We
              excavate down to the aggregate in the absorption area to inspect
              the stone and liquid level and also check the distribution boxes.
              Once the system is fully inspected, conclusions can be made with
              recommendations about the septic system's operation which
              determines whether the system in question will be able to serve
              the future needs of your family.
              <br />
              <br />
              If a problem is identified, we can help with referrals to repair
              services and direct you to helpful resources. We will work
              diligently with the local authorities and ensure your septic
              system is in the hands of qualified professionals who can restore
              it to its optimal working order to pass inspection. Once you
              receive your fully comprehensive report, no follow-up is needed
              but feel free to contact us if anything arises.
            </v-card-text>
          </v-card>
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
