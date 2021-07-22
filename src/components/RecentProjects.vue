<template>
  <section id="recent-projects" class="hide-overflow">
    <v-layout white>
      <v-flex hidden-sm-and-down md6 >
        <v-img :src="require('@/assets/keyboard.jpg')" height="100%"/>
      </v-flex>

      <v-flex xs12 md6 primary text-xs-center pa-5 white--text>
        <base-heading>
          Recent Projects
        </base-heading>

        <base-text class="mb-5">
          These are some of the projects that I've worked on.<br>
            Feel free to look around and reach out to me if you want to connect.
        </base-text>

        <v-card color="secondary">
          <v-container grid-list-md pa-2>
            <v-layout wrap>
              <v-flex v-for="(project, i) in projects" :key="i" xs12 md6>

            <span>
              <v-card-text class="text-center grey--text text--darken-3 font-weight-medium body-1">
                <a :href="project.url">
                  <h3>{{project.name}}</h3>
                </a>
              </v-card-text>

              <v-card-actions>
                <v-layout mb-1 justify-center>
                  <v-tooltip bottom color="black">
                    <template v-slot:activator="{ on }">
                      <a :href="project.github">
                        <v-icon x-large color="black" v-on="on" class="fab fa-github"></v-icon>
                      </a>
                    </template>
                    <span>{{project.label}}</span>
                  </v-tooltip>
                </v-layout>
              </v-card-actions>
            </span>

              <v-tooltip top color="black">
                <template v-slot:activator="{ on }">
                  <a :href="project.url">
                    <v-img :src="require(`@/assets/projects/${project.logo}`)" aspect-ratio="1" :alt="project.alt" v-on="on"></v-img>
                  </a>
                </template>
                <span>{{project.alt}}</span>
              </v-tooltip>

              </v-flex>
            </v-layout>
          </v-container>
        </v-card>
      </v-flex>
    </v-layout>
  </section>
</template>

<script>
export default {
  data: () => ({
    projects: [
        {
          id: 1,
          name: "Portfolio Website",
          logo: "portfolio.png",
          url: "https://jasongedamke.com",
          github: "https://github.com/jaswged/gedamke-website",
          alt: "Where I showcase and talk about myself",
          label: "Portfolio Website's GitHub"
        },
        {
          id: 2,
          name: "Die Detector",
          logo: "die-detector-api.png",
          url: "http://diedetector-env.eba-ypymk3gb.us-east-2.elasticbeanstalk.com/",
          github: "https://github.com/jaswged/die-detector-api",
          alt: "Machine Learning Detector for which type of die the image is of",
          label: "Die Detector Api's GitHub"
        },
        {
          id: 3,
          name: "Sorting Visualizer",
          logo: "SortingVisualizer.png",
          url: "https://jasongedamke.com",
          github: "https://github.com/jaswged/vue_sorting_visualizer",
          alt: "Visualizer for sorting algorithms built on Vue.js",
          label: "Visualizer for sorting algorithms built on Vue.js"
        },
        {
          id: 4,
          name: "Mancala AI, reinforcement learning",
          logo: "Mancala-ai-logo.png",
          url: "https://jasongedamke.com",
          github: "https://github.com/jaswged/mancala-ai",
          alt: "AI for playing Mancala trained with reinforcement learning",
          label: "AI for playing Mancala trained with reinforcement learning"
        },
        {
          id: 5,
          name: "My Games on Itch",
          logo: "itch.png",
          url: "https://galacticinsight.itch.io/",
          github: "https://github.com/jaswged",
          alt: "Link to my itch page for my indie games",
          label: "Indie games on Itch"
        }       
    ]
  })
}
</script>
<style>
  .v-application .primary{
    background-color: #424242 !important;
    border-color: #0064A2 !important;
  }
.v-application a{
      color: #ffffff;
      text-decoration: none;
}
</style>
