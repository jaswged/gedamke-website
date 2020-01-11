<template>
  <section id="welcome" class="hide-overflow" >
    <v-layout>
      <v-flex hidden-sm-and-down md6 >
        <v-img :src="require('@/assets/welcome.png')" height="100vh" />
      </v-flex>

      <v-flex xs12 md6 align-content-space-between layout :pa-5="$vuetify.breakpoint.smAndDown" wrap >
        <v-layout column fill-height align-center justify-center>
          <v-flex xs1 class="display-4 text-center font-weight-medium">
            <div class="new-font text-center font-weight-medium mb4">Jason Gedamke</div>
            <v-tooltip left>
              <template v-slot:activator="{ on }">
                <a href="https://linkedin.com/in/jasonwgedamke">
                  <v-icon x-large color="blue" v-on="on" class="mx-3 fab fa-linkedin"></v-icon>
                </a>
              </template>
              <span>LinkedIn</span>
            </v-tooltip>
            <v-tooltip top>
              <template v-slot:activator="{ on }">
                <a href="https://github.com/jaswged">
                  <v-icon x-large color="black" v-on="on" class="mx-3 fab fa-github"></v-icon>
                </a>
              </template>
              <span>GitHub</span>
            </v-tooltip>
            <v-tooltip right>
              <template v-slot:activator="{ on }">
                <a href="mailto:jaswged@gmail.com">
                  <v-icon x-large color="red lighten-1" v-on="on" class="mx-3 fas fa-envelope"></v-icon>
                </a>
              </template>
              <span>Email</span>
            </v-tooltip>

            <v-flex>
              <!-- <a href="../../assets/resources/GedamkeResume.pdf" download> -->
              <!-- <v-btn href="https://docs.google.com/document/d/1WSR42FEgUahJuR_RArW1wz7TfUBlgj13zekRidmQgs4/edit?usp=sharing"                      target="_blank" color="green" dark large> -->
                <v-btn large color="secondary" rounded target="_blank" href="https://drive.google.com/open?id=1Ux3Olw4_cYYro9hKqFs2YrhLAa29mg9slmJVIBMweIw">
                  <span class="mr-2">Download Resume
                    <em class="fa fa-download"></em>
                  </span>
                </v-btn>
              <!-- </a> -->
            </v-flex>            

            <div class="display-1">
              <span class="new-font">Data Architect</span>
              <br />
              <span class="new-font">Full Stack Developer</span>
              <br />
              <span class="new-font">Lifelong Learner</span>
            </div>
          </v-flex>
        </v-layout>
      </v-flex>
    </v-layout>
  </section>
</template>
<style scoped>
.v-application a{
      color: #ffffff;
}
</style>