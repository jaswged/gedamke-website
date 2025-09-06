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
            "Engineer multithreaded Rust pipelines to process 100M+ JSON files, enabling relational querying in Snowflake",
            "Automate ingestion of S3 event streams with SQS and Fargate, enabling near-real-time data availability",
            "Reimplement high-throughput AWS Lambda services in Rust, cutting compute costs by 50%",
            "Accelerate decision-making with enterprise data marts supporting millions of credit card transactions",
            "Achieve billion-row data processing capacity through scalable data pipeline optimization using Python and DBT",
            "Improve financial data accessibility by deploying AI chatbots with Llama and RAG architecture",
            "Craft data quality assurance test suites using Polars and DuckDB"
          ]
        },
        {
          id: 2,
          company: "Blast Motion",
          title: "Senior Software Engineer",
          dates: "August 2021 - June 2023",
          outcomes: [
            "Streamed 6B+ transactions from DynamoDb to data lake using Kinesis and PySpark for real-time analysis",
            "Produced ML models for impact detection and player classification, enhancing product insights",
            "Delivered real-time sports analytics to MLB teams through high-availability APIs fronted by API Gateway",
            "Wrote C# .NET lambdas to interconnect APIS to SQS queues and DynamoDb to improve system reliability",
            "Standardized AWS infrastructure with Terraform modules, ensuring reproducibility across environments"
          ]
        },
        {
          id: 3,
          company: "Northcentral Technical College",
          title: "Adjunct Instructor",
          dates: "August 2019 - May 2021",
          outcomes: [
            "Lecture 'Database Design and SQL' both in person and online via CANVAS",
            "Professor for 'Programming Concepts with C#'"
          ]
        },  
        {
          id: 4,
          company: "Church Mutual Insurance Company",
          title: "Advisory New Application Developer",
          dates: "December 2014 - August 2021",
          outcomes: [
            "Architected an enterprise data warehousing program with change data capture and ETL",
            "Modernized enterprise data strategy with CDC-driven architecture, enabling timely insights for BI",
            "Profiled corporate data using Python and pandas for statistics, metrics and patterns",
            "Developed and governed corporate wide data integrations with Java REST APIs",
            "Reduced IT operating costs by $40K annually by spearheading a migration away from WebSphere"
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