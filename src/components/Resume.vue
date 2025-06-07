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
          company: "Cross River Bank",
          title: "Senior Data Engineer",
          dates: "July 2023 - Present",
          outcomes: [
            "Build out AWS data platform using Airflow and DBT",
            "Design an enterprise data mart in Snowflake for lending data and credit card transactions",
            "Create AI chat-bots using rag and Llama models for balance sheet finance data",
            "Parse over 100 million json and parquet files into a relational data format using rust"
          ]
        },
        {
          id: 2,
          company: "Blast Motion",
          title: "Senior Software Engineer",
          dates: "August 2021 - June 2023",
          outcomes: [
            "Build out Datalake using AWS glue, PySpark and Iceberg/HUDI tables with over 2 billion rows",
            "Develop and maintain API's used by the majority of Major League Baseball teams",
            "Generate dashboards in ElasticSearch and AWS Quicksight to support business intelligence",
            "Stream transactional data from DynamoDb to data lake using kinesis and glue for real time analytics",
            "Produce Machine Learning models for impact detection and level of play classification with SageMaker",
            "Build Terraform modules for AWS infrastructure to have reproducibility across environments"
          ]
        },
        {
          id: 3,
          company: "Northcentral Technical College",
          title: "Adjunct Instructor",
          dates: "August 2019 - May 2021",
          outcomes: [
            "Lecture Database Design and SQL both in person and online via CANVAS",
            "Professor for Programming Concepts with C#"
          ]
        },  
        {
          id: 4,
          company: "Church Mutual Insurance Company",
          title: "Advisory New Application Developer",
          dates: "October 2018 - August 2021",
          outcomes: [
            "Tech lead for a new Data Warehousing program, both architecture and design",
            "Create relational models from flat files, including xml, using Informatica",
            "Develop and govern corporate wide data integrations with a Java REST API",
            "Used python and pandas for quick prototyping and data profiling of statistics and patterns",
            "Utilized Azure devops with git for continuous integration and deployment (CICD)"
          ]
        },
        {
          id: 5,
          company: "Church Mutual Insurance Company",
          title: "New Application Developer",
          dates: "December 2014 - October 2018",
          outcomes: [
            "Modeled Enterprise Data Warehouse for insurance policy and premium data",
            "Mentored and oversaw summer interns on Broker Management agile project",
            "Designed and created Account Master database",
            "Integrated a new policy Admin system for Worker Compensation policies",
            "Spearheaded replacement of WebSphere saving $41,000 per year on licensing",
            "Rewrote the underwriting workflow system for document processing"
          ]
        },
        {
          id: 6,
          company: "University of Wisconsin - Stevens Point",
          title: "Bachelor of Science",
          dates: "August 2009 - December 2014",
          outcomes: [
            "Major: Computer Information Systems"
          ]
        },
        {
          id: 7,
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
          id: 8,
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
          id: 9,
          company: "Church Mutual Insurance Company",
          title: "IT Intern, Java Developer",
          dates: "May - August 2014",
          outcomes: [
            "Designed and developed a Data Dictionary Java app with a db2 backend",
            "Modeled and constructed entire data base backend",
            "Executive presentation of project and overall experience"
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