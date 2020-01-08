<template>
  <section id="about" class="hide-overflow">
    <v-layout white>
      <v-flex xs12 md6 pa-5>
        <v-layout column fill-height align-center justify-center>
          <base-heading class="whiter">
            About Me
          </base-heading>

          <base-text class="mb-5 whiter">
            Hello, I'm Jason Gedamke. This site is a collection of information about me and some of my projects.
          </base-text>

          <base-subheading class="whiter">
            Hobbies
          </base-subheading>

          <v-alert outlined color="info">
            <v-layout v-for="(interest, i) in interests" :key="i" style="color: #69A1BB;" wrap>
              <v-flex xs6 text-uppercase whiter v-text="interest.name" />
              <v-flex pt-2 xs6 text-xs-right whiter v-text="`${interest.body}`" />
            </v-layout>
          </v-alert>
        </v-layout>
      </v-flex>

      <v-flex hidden-sm-and-down md6 >
        <v-img :src="require('@/assets/pilot.png')" height="100%"/>
      </v-flex>
    </v-layout>
  </section>
</template>

<script>
export default {
  data: () => ({
    interests: [
      {
        name: "Software Development",
        body:
          "Software development has always been a fascinating topic to me. The way that you can give \"Commands\" to a machine and achieve amazing things, is just incredible. Especially when you remember that the cpu in the computer is just a rock that we tricked into thinking with science!"
      },
      {
        name: "Powerlifting",
        body:
          "Recently I got back into lifting weights and I chose to emphasize strength over aesthetics. My current maxes are 465 Deadlift, 325 Squat and 275 Bench press."
      },
      {
        name: "Flying",
        body: "I am a student pilot who looks forward to finishing their private pilots license sometime in the future. I've flown a Beechcraft Sundowner and a Cessna 172"
      }
    ]
  })
}
</script>
<style>
  .v-application .info--text{
    background-color: #424242 !important;
    border-color: #FFFFFF !important;
  }
  .v-application .white {
    background-color: #424242 !important;
    border-color: #FFFFFF !important;
  }

  .whiter {
    color: #FFFFFF !important;
  }
</style>