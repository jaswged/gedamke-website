<template>
  <section id="welcome" class="hide-overflow"
  >
    <v-layout>
      <v-flex hidden-sm-and-down md6 >
        <v-img :src="require('@/assets/welcome.png')" height="100vh" />
      </v-flex>

      <v-flex xs12 md6 align-content-space-between layout :pa-5="$vuetify.breakpoint.smAndDown" wrap >
        <base-chip-1 style="transform: rotate(180deg) translate(5px, 37%)"/>

        <v-layout align-center justify-center>
          <v-flex xs10  md6 >
            <base-heading>Jason Gedamke</base-heading>
            <base-text>
              Hello, I'm Jason Gedamke. This site is a collection of information about me and some of my projects.
              <br>
              On this site I post projects that I've worked on, as well as things I'm interested in. 
              Feel free to look around or reach out to me if you want to connect.
            </base-text>
            <base-btn large class="mt-4" target="_blank" href="https://docs.google.com/document/d/1WSR42FEgUahJuR_RArW1wz7TfUBlgj13zekRidmQgs4/edit?usp=sharing">
              Download Resume
              <em class="fa fa-download"></em>
            </base-btn>
          </v-flex>
        </v-layout>

        <base-chip-2 style="transform: rotate(180deg) translate(-75px, -27%)"/>
      </v-flex>
    </v-layout>
  </section>
</template>

<style scoped>

</style>
