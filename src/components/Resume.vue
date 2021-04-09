<template>
  <header>
    <link
      rel="stylesheet"
      href="https://cdn.jsdelivr.net/gh/devicons/devicon@v2.10.1/devicon.min.css"
    />
  </header>
  <body>
    <div class="resumeText" :style="{ color: textColor }">
      <h1>Who am I?</h1>
      <p>
        I'm a student from Copenhagen, Denmark pursuing a career in the tech
        industry. I'm fluent in English, German and Danish. <br />
        I'm a former Danish national team rower and current full time student
        athlete. I possess excellent teamwork, communication and collaboration
        skills. <br />
        I am a fast learner with strong work ethics and a dedication to problem
        solving.
      </p>

      <div id="education">
        <h2>Education</h2>
        <h4>
          B.A. <b>Computer Science</b> at
          <i><b>Boston University</b>, Boston, Massachusetts, USA,</i> Class of
          <b>2022</b>
        </h4>
        <div class="col-xs-6">
          <h4><b>Relevant courses:</b></h4>
          <ul>
            <li :key="subject" v-for="subject in classes">{{ subject }}</li>
          </ul>
        </div>
        <div class="col-xs-6">
          <h4><b>Programming languages include:</b></h4>
          <i class="devicon-c-line"></i>
          <i class="devicon-java-plain colored"></i>
          <i class="devicon-python-plain colored"></i>
          <i class="devicon-html5-plain colored"></i>
          <i class="devicon-css3-plain colored"></i>
          <i class="devicon-javascript-plain colored"></i>
          <i class="devicon-vuejs-plain colored"></i>
          <ul>
            <li :key="language" v-for="language in programmingLanguages">
              {{ language }}
            </li>
          </ul>
        </div>
      </div>
      <br />

      <div id="accomplishments">
        <h2>Accomplishments</h2>
        <div class="col-xs-6">
          <h4><b>Danish National Rowing Team:</b></h4>
          <ul>
            <li class="left"><b>2015</b>, <i>U18, Baltic Cup</i>, 5th place</li>
            <br />
            <li class="left">
              <b>2016</b>, <i>U19, European Rowing Championships</i>, 5th place
            </li>
            <br />
            <li class="subleft">
              <i>U19, World Rowing Championships</i>, 11th place
            </li>
            <br />
            <li class="left">
              <b>2017</b>, <i>U19, European Rowing Championships</i>, 5th place
            </li>
            <br />
            <li class="subleft">
              <i>U19, World Rowing Championships</i>, 7th place
            </li>
            <br />
            <li class="left">
              <b>2018</b>, <i>U23, World Rowing Championships</i>, 10th place
            </li>
            <br />
          </ul>
        </div>

        <div class="col-xs-6">
          <h4><b>Boston University Men's Crew:</b></h4>
          <ul>
            <li class="left">
              <b>2018</b>, <i>Head of the Charles Regatta</i>, MA, USA
            </li>
            <br />
            <li class="left"><b>2019</b>, <i>Windermere Cup</i>, WA, USA</li>
            <br />
            <li class="subleft"><i>Eastern Sprints Regatta</i>, MA, USA</li>
            <br />
            <li class="subleft">
              <i>IRA National Championship Regatta</i>, CA, USA
            </li>
            <br />
            <li class="subleft"><i>Henley Royal Regatta</i>, Henley, UK</li>
            <br />
            <li class="subleft"><i>Head of the Charles Regatta</i>, MA, USA</li>
            <br />
          </ul>
        </div>
      </div>

      <div id="contact">
        <h2>Contact</h2>
        <div class="row">
          <div class="col-xs-4">
            <p><b>E-mail:</b> eskok@bu.edu</p>
          </div>
          <div class="col-xs-4">
            <div id="divfix">
              <a
                href="https://www.linkedin.com/in/esben-s%C3%B8vndahl-kok-bb55711b8/"
                target="_blank"
                ><svg
                  xmlns="http://www.w3.org/2000/svg"
                  width="24"
                  height="24"
                  fill="currentColor"
                  class="bi bi-linkedin"
                  viewBox="0 0 16 16"
                >
                  <path
                    d="M0 1.146C0 .513.526 0 1.175 0h13.65C15.474 0 16 .513 16 1.146v13.708c0 .633-.526 1.146-1.175 1.146H1.175C.526 16 0 15.487 0 14.854V1.146zm4.943 12.248V6.169H2.542v7.225h2.401zm-1.2-8.212c.837 0 1.358-.554 1.358-1.248-.015-.709-.52-1.248-1.342-1.248-.822 0-1.359.54-1.359 1.248 0 .694.521 1.248 1.327 1.248h.016zm4.908 8.212V9.359c0-.216.016-.432.08-.586.173-.431.568-.878 1.232-.878.869 0 1.216.662 1.216 1.634v3.865h2.401V9.25c0-2.22-1.184-3.252-2.764-3.252-1.274 0-1.845.7-2.165 1.193v.025h-.016a5.54 5.54 0 0 1 .016-.025V6.169h-2.4c.03.678 0 7.225 0 7.225h2.4z"
                  />
                </svg>
              </a>
            </div>
          </div>
          <div class="col-xs-4">
            <div id="divfix">
              <a href="https://github.com/esbensoevndahl" target="_blank"
                ><svg
                  xmlns="http://www.w3.org/2000/svg"
                  width="24"
                  height="24"
                  fill="currentColor"
                  class="bi bi-github"
                  viewBox="0 0 16 16"
                >
                  <path
                    d="M8 0C3.58 0 0 3.58 0 8c0 3.54 2.29 6.53 5.47 7.59.4.07.55-.17.55-.38 0-.19-.01-.82-.01-1.49-2.01.37-2.53-.49-2.69-.94-.09-.23-.48-.94-.82-1.13-.28-.15-.68-.52-.01-.53.63-.01 1.08.58 1.23.82.72 1.21 1.87.87 2.33.66.07-.52.28-.87.51-1.07-1.78-.2-3.64-.89-3.64-3.95 0-.87.31-1.59.82-2.15-.08-.2-.36-1.02.08-2.12 0 0 .67-.21 2.2.82.64-.18 1.32-.27 2-.27.68 0 1.36.09 2 .27 1.53-1.04 2.2-.82 2.2-.82.44 1.1.16 1.92.08 2.12.51.56.82 1.27.82 2.15 0 3.07-1.87 3.75-3.65 3.95.29.25.54.73.54 1.48 0 1.07-.01 1.93-.01 2.2 0 .21.15.46.55.38A8.012 8.012 0 0 0 16 8c0-4.42-3.58-8-8-8z"
                  />
                </svg>
              </a>
            </div>
          </div>
        </div>
      </div>
    </div>
  </body>
</template>

<script>
export default {
  data() {
    return {
      textColor: "grey",
      classes: [
        "Computer Systems",
        "Operating Systems",
        "Software Engineering",
        "Analysis of Algorithms",
        "Concepts of Programming Languages",
      ],
      programmingLanguages: [
        "C",
        "Java",
        "Ocaml",
        "Python",
        "HTML/CSS",
        "JavaScript and Vue.js",
      ],
    };
  },
};
</script>

<style scoped>
ul {
  list-style-type: none;
}
.left {
  position: absolute;
  margin-left: 200px;
}
.subleft {
  position: absolute;
  margin-left: 240px;
}
body {
  overflow-x: hidden;
}
.resumeText{
    display: block;
    margin-left: 100;
    margin-right: 100;
}
</style>