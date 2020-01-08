<template>
  <section id="recent-projects" class="hide-overflow">
    <v-layout white>
      <v-flex hidden-sm-and-down md6 >
        <v-img :src="require('@/assets/background.jpg')" height="100%"/>
      </v-flex>

      <v-flex xs12 md6 primary text-xs-center pa-5 white--text>
        <base-heading>
          Recent Projects
        </base-heading>

        <base-text class="mb-5">
          On this site I post projects that I've worked on, as well as things I'm interested in. <br>
            Feel free to look around or reach out to me if you want to connect.
        </base-text>

        <v-card color="secondary">
          <v-container grid-list-md pa-2>
            <v-layout wrap>
              <v-flex v-for="(project, i) in projects" :key="i" xs12 md6>
                <a href="#">
                  <v-img :src="require(`@/assets/projects/${project.logo}`)" max-height="300"/>
                </a>
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
          github: "https://github.com/jaswged/portfolio-website",
          alt: "Where I showcase and talk about myself",
          label: "Portfolio Website's GitHub"
        },
        {
          id: 2,
          name: "Die Detector",
          logo: "portfolio.png",
          url: "https://jasongedamke.com",
          github: "https://github.com/jaswged/portfolio-website",
          alt: "Where I showcase and talk about myself",
          label: "Portfolio Website's GitHub"
        },
        {
          id: 3,
          name: "Sorting Visualizer",
          logo: "itch.jpg",
          url: "https://galacticinsight.itch.io/",
          github: "https://github.com/jaswged",
          alt: "Link to my itch page for my indie games",
          label: "Indie games on Itch"
        },
        {
          id: 4,
          name: "Games on Itch",
          logo: "itch.jpg",
          url: "https://galacticinsight.itch.io/",
          github: "https://github.com/jaswged",
          alt: "Link to my itch page for my indie games",
          label: "Indie games on Itch"
        },
        {
          id: 5,
          name: "Mancala AI, reinforcement learning",
          logo: "itch.jpg",
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
</style>
