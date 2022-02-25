<template>
  <section id="resume" class="hide-overflow">
    <v-layout info white--text >
      <v-flex xs12 md6 pa-5 >
        <v-expansion-panels>
          <v-expansion-panel v-for="(experience,ind) in experiences" :key="ind">
            <v-expansion-panel-header>
              <v-layout>
                <v-flex class="xs4 body-1 text-left hidden-sm-and-down">
                  <strong>{{experience.company}}</strong>
                </v-flex>
                <v-flex class="xs4 body-1 text-center hidden-sm-and-down">
                  <i>{{experience.dates}}</i>
                </v-flex>
                <v-flex class="pr-3 xs4 body-1 text-right hidden-sm-and-down">
                  <strong>{{experience.title}}</strong>
                </v-flex>
                <v-flex class="xs5 body-2 text-left hidden-md-and-up">
                  <strong>{{experience.company}}</strong>
                </v-flex>
                <v-flex pr-3 class="xs7 body-2 text-center hidden-md-and-up">
                  <strong>{{experience.title}}</strong>
                  <br />
                  <i>({{experience.dates}})</i>
                </v-flex>
            </v-layout>  
            </v-expansion-panel-header>
            <v-expansion-panel-content>
              <ul>
                <li class="body-1 hidden-sm-and-down" v-for="(outcome, index) in experience.outcomes" :key="index">
                  {{outcome}}
                </li>
                <li class="body-2 hidden-md-and-up" v-for="(outcome, index) in experience.outcomes" :key="index">
                  {{outcome}}
                </li>
              </ul>
            </v-expansion-panel-content>
          </v-expansion-panel>
        </v-expansion-panels>
      </v-flex>

      <v-flex hidden-sm-and-down md6>
        <v-img :src="require('@/assets/Mount_Hood.jpg')" height="100%"/>
      </v-flex>
    </v-layout>
  </section>
</template>
<script>
export default {
  data() {
    return {
      experiences: [
        {
          id: 1,
          company: "Blast Motion",
          title: "Senior Software Engineer",
          dates: "August 2021 - Present",
          outcomes: [
            "ETL for Datalake using AWS glue and PySpark",
            "Use SageMaker to generate predictive models",
            "Provide feedback on student database designs"
          ]
        },
        {
          id: 2,
          company: "Northcentral Technical College",
          title: "Adjunct Instructor",
          dates: "August 2019 - Present",
          outcomes: [
            "Lecture Database Design and SQL both in person and online via CANVAS",
            "Assisted in course and competency rewrite for the data curriculum",
            "Provide feedback on student database designs"
          ]
        },  
        {
          id: 3,
          company: "Church Mutual Insurance Company",
          title: "Advisory New Application Developer",
          dates: "October 2018 - August 2021",
          outcomes: [
            "Tech lead for a new Data Warehousing program, both architecture and design",
            "Create relational models from flat files, including xml, using Informatica",
            "Develop and govern corporate wide data integrations with a Java REST API",
            "Sit on application design approval board with architecture"
          ]
        },
        {
          id: 4,
          company: "Church Mutual Insurance Company",
          title: "New Application Developer",
          dates: "December 2014 - October 2018",
          outcomes: [
            "Modeled Enterprise Data Warehouse for insurance policy and premium data",
            "Mentored and oversaw summer interns on Broker Management agile project",
            "Designed and created Account Master database",
            "Created a profiling tool to determine counts, patterns, and statistics of data",
            "Integrated a new policy Admin system for Worker Compensation policies",
            "Spearheaded replacement of WebSphere saving $41,000 per year on licensing",
            "Rewrote the underwriting workflow system for document processing"
          ]
        },
        {
          id: 5,
          company: "University of Wisconsin - Stevens Point",
          title: "Bachelor of Science",
          dates: "August 2009 - December 2014",
          outcomes: [
            "Major: Computer Information Systems"
          ]
        },
        {
          id: 6,
          company: "UWSP Tutoring and Learning Center",
          title: "Technology Tutor",
          dates: "August - December 2014",
          outcomes: [
            "Explained complex concepts to fellow programming students",
            "Provided one on one training on software development and database topics",
            "Assisted with adoptions of new educational technologies such as smart boards",
            "Taught Classes about new technologies and tools such as Visual Studio"
          ]
        },
        {
          id: 7,
          company: "Sentry Insurance",
          title: "Senior Capstone Externship",
          dates: "August - December 2014",
          outcomes: [
            "Rewrote and improved an old VB.Net app using struts 2 and DAO architecture",
            "Created database backend for an Archive File Tracking System",
            "Used abstraction and inheritance for type independence "
          ]
        },
        {
          id: 8,
          company: "Church Mutual Insurance Company",
          title: "IT Intern, Java Developer",
          dates: "May - August 2014",
          outcomes: [
            "Designed and developed a Data Dictionary Java app with a db2 backend",
            "Modeled and constructed entire data base backend",
            "Executive presentation of project and overall experience"
          ]
        },
        {
          id: 9,
          company: "UWSP Planetarium and Observatory",
          title: "Planetarium and Observatory lecturer",
          dates: "November 2009 - May 2011",
          outcomes: [
            "Lectured groups up to 60 people about the wonders of Astronomy and Physics",
            "Enlightened people about the wonders of Astronomy and Physics",
            "Kept equipment up to date and in working order",
            "Orchestrated laser shows to music"
          ]
        }
      ]
    };
  }
};
</script>
<style scoped>
.experience-color {
  background-color: #000f08;
}
</style>