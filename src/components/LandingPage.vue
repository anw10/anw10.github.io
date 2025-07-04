<template>
  <div>
    <div class="d-flex justify-content-center ml-2">
      <b-avatar src="../assets/arsalan.jpg" size="10rem"></b-avatar>
      <div class="d-flex align-items-center m-4" :style="{ fontSize: '2rem' }">
        <a>Arsalan Bin Najeeb Wyne</a>
      </div>
    </div>
    <!-- Headers -->
    <div class="m-4">
      <b-card>
        <b-card-text class="d-inline-block">
          <b-link class="d-inline-block mx-4" href="abnajeeb@knox.edu"
            ><b-icon-mailbox class="mr-2" />arsalannajeeb0@gmail.com</b-link
          >
          <b-link class="d-inline-block mx-4" href="https://github.com/anw10"
            ><b-icon-github class="mr-2" />anw10</b-link
          >
          <b-link
            class="d-inline-block mx-4"
            href="https://www.linkedin.com/in/arsalanwyne/"
            ><b-icon-linkedin class="mr-2" />arsalanwyne</b-link
          >
        </b-card-text>
      </b-card>
      <b-card class="mt-2" title="About Me">
        <b-card-text class="d-inline-block"
          >Thank you for visiting, I recently completed my Masters in Computer
          Science from George Washington University. In my free time I mostly
          hike and try creating new recipes
          <span>&#127802;</span>
        </b-card-text>
      </b-card>
    </div>
    <!-- Research -->
    <div>
      <div class="d-flex justify-content-between mx-4">
        <h2 class="align-self-center">Research</h2>
        <div class="clickable">
          <b-icon-patch-plus
            v-b-toggle.research
            class="align-self-center"
            style="border-color: red"
            animation="spin"
            font-scale="2"
          ></b-icon-patch-plus>
        </div>
      </div>
      <b-collapse id="research" class="mt-2">
        <b-card class="m-4">
          <b-card-title>Weak to Strong Alignment</b-card-title>
          <b-card-text class="d-inline-block"
            >Implemented and investigated the affects of Weak to Strong
            Alignment by using BERT and GPT-4o. Presented my findings at GWU
            through their AI special topics platform. Also evaluated the
            consequences of using Weak to Strong Alignment on the safety of the
            final Strong model by running tests on the SST2 benchmark.
          </b-card-text>
          <b-button
            variant="outline-dark"
            style="color: purple; border-color: purple; background-color: white"
            href="https://github.com/anw10/W2S_Safety"
            >Open Repo</b-button
          >
        </b-card>
        <b-card class="m-4">
          <b-card-title>Rust Benchmarking</b-card-title>
          <b-card-text class="d-inline-block"
            >In progress research project to create a universal benchmarking
            tool for Safe & Unsafe Rust. Developed by using custom LLVM passes
            and a thorough understanding of the Rust compiler. The goal is to
            create a tool that can be used to benchmark any Rust code and
            provide insights into its performance such as the SPEC becnhmarking
            tool.
          </b-card-text>
        </b-card>
        <b-card class="m-4">
          <b-card-title>South Asian Computing</b-card-title>
          <b-card-text class="d-inline-block"
            >My co-authored publication for ICER 2020 investigates the enacted
            computing curriculum and its various side affects for South Asian's.
            We gathered and compiled data relating to CS-ED and where the
            curriculum currently stands for countries that have little to none
            representation from Asia as a whole and more specifically South
            Asia.
          </b-card-text>
          <b-button
            variant="outline-dark"
            style="color: purple; border-color: purple; background-color: white"
            href="https://dl.acm.org/doi/10.1145/3372782.3406251"
            >Open Paper</b-button
          >
        </b-card>
        <b-card class="m-4">
          <b-card-title>ToUCH</b-card-title>
          <b-card-text class="d-inline-block"
            >ToUCH is a collaborative project between Texas State University,
            Concordia University and Knox College, this is an NSF funded
            project. We developed novel teaching materials for undergraduate
            students on how to program and use Heterogeneous Computing Systems.
            We are using a combination of Heterogeneous systems for our
            materials such as the Raspberry Pi and mobile phones based on the
            ARM big.LITTLE architecture and supercomputing systems with Nvidia
            cards that support CUDA programming. I was a part of the first team
            that setup the project and started development on course materials
            while at Knox. </b-card-text
          ><b-icon-file-earmark-spreadsheet
            v-b-toggle.tCollapse
            scale="1.5"
            class="mb-2"
          ></b-icon-file-earmark-spreadsheet
          ><b-collapse id="tCollapse"
            ><iframe
              width="100%"
              height="auto"
              style="zoom: 2"
              :src="`${publicPath}Poster_RPI.pdf`"
            ></iframe></b-collapse></b-card
        ><b-card class="m-4">
          <b-card-title>Dragonfly</b-card-title>
          <b-card-text class="d-inline-block"
            >Dragonfly is a High Performance Computer topology, our project was
            funded by an NSF grant. Working alongside one other student and our
            advisor Prof. David Bunde, we developed an algorithm to map tasks
            onto a dragonfly system. I presented our work at various conferences
            and at the 2018 Consortium of Computing Science Colleges: MidWest
            Conference we were awarded 1st place for our work. </b-card-text
          ><b-icon-file-earmark-spreadsheet
            v-b-toggle.dCollapse
            scale="1.5"
            class="mb-2"
          ></b-icon-file-earmark-spreadsheet
          ><b-collapse id="dCollapse"
            ><iframe
              width="100%"
              height="auto"
              style="zoom: 2"
              :src="`${publicPath}Poster_Dragonfly.pdf`"
            >
            </iframe>
          </b-collapse>
        </b-card>
      </b-collapse>
    </div>
    <!-- Experiences -->
    <div>
      <div class="d-flex justify-content-between mx-4">
        <h2>Experiences</h2>
        <b-icon-patch-plus
          v-b-toggle.experiences
          class="align-self-center"
          font-scale="2"
        ></b-icon-patch-plus>
      </div>
      <b-collapse id="experiences" class="mt-2"
        ><b-card class="m-4"
          ><b-card-title>Work Experiences</b-card-title
          ><b-card-body
            >Software Engineer Intern (Part Time) -- Incentifind, Inc
            <b>|</b> PHP, GraphQL, Laravel, React, SQLSRV, AWS, Sentry, Forge<br /><br />
            Software Engineer -- TWST Events (Acquisition of CSS) <b>|</b> Java,
            Groovy, Grails, MySQL, Postgres, Firebase, Next.js, Vue.js, React,
            Apache, Perl, AWS, GCP <br /><br />
            Full-Stack Developer -- StreamEngine.io <b>|</b> Python, Django,
            React <br /></b-card-body
        ></b-card>
        <b-card class="m-4"
          ><b-card-title>Academic Experiences</b-card-title
          ><b-card-body
            >Graduate Teaching Assistant for Advanced Machine Learning Courses
            <b>|</b> Graduate Research Assistant <b>|</b> School of Engineering
            and Applied Science Ambassador <br /><br />
            Teaching Assistant for 4 courses in Java; Object Oriented
            Programming, Data Structures (Maps, Arrays, Linked Lists, Trees,
            Stacks), Algorithm Design & Analysis (BFS/DFS, A*, Sorting, Binary
            Search), Programming Languages
            <b>|</b> Resident Assistant Feb 2018 - Jun 2019 <b>|</b> Alumni
            Ambassador President Mar 2017 - Jun 2020 <b>|</b> Computer Science
            Tutor Sept 2017 - Jun 2020 <b>|</b> Orientation Leader Aug 2017 -
            Sept 2017
          </b-card-body></b-card
        ></b-collapse
      >
    </div>
    <!-- Projects -->
    <div>
      <div class="d-flex justify-content-between mx-4">
        <h2>Projects</h2>
        <b-icon-patch-plus
          v-b-toggle.projects
          class="align-self-center"
          font-scale="2"
        ></b-icon-patch-plus>
      </div>
      <b-collapse id="projects" class="mt-2"
        ><b-card class="m-4">
          <b-card-title>Zing </b-card-title>
          <b-card-text class="d-inline-block"
            >Cross Platform iOS and Android application made using React Native
            and Firebase. This was my startup venture that provides a solution
            for finding events near you that are catered to your interests.
          </b-card-text>
        </b-card>
        <b-card class="m-4">
          <b-card-title>B.L.O.B </b-card-title>
          <b-card-text class="d-inline-block"
            >Android application made using Unity, team based project for CS
            292. Work was divided into 3 sprints each a week long and our
            overall goal was to incorporate awareness of climate change into it.
          </b-card-text>
        </b-card>
        <b-card class="m-4">
          <b-card-title>Scrub </b-card-title>
          <b-card-text class="d-inline-block"
            >Cross Platform iOS and Android application made using React Native
            and Expo development stack. Scrub teaches you the correct way to
            wash your hands as suggested by the CDC and WHO. App is also hosted
            as a snack.
          </b-card-text>
        </b-card>
      </b-collapse>
    </div>
    <!-- Resume -->
    <div class="mb-4">
      <div class="d-flex justify-content-between mx-4">
        <h2>Resume</h2>
        <b-icon-patch-plus
          v-b-toggle.resume
          class="align-self-center"
          font-scale="2"
        ></b-icon-patch-plus>
      </div>

      <b-collapse id="resume" class="mt-2">
        <b-card class="m-4">
          <iframe
            width="100%"
            height="450em"
            style="zoom: 2"
            :src="`${publicPath}ArsalanBinNajeeb_Resume.pdf`"
          ></iframe>
        </b-card>
      </b-collapse>
    </div>
  </div>
</template>

<script>
export default {
  name: "LandingPage",
  components: {},
  data() {
    return {
      publicPath: process.env.BASE_URL,
      topened: false,
    };
  },

  computed: {},
  methods: {
    customeAnimation() {
      return "";
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss"></style>
