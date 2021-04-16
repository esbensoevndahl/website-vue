<template>
  <header>
    <link
      rel="stylesheet"
      href="https://cdn.jsdelivr.net/gh/devicons/devicon@v2.10.1/devicon.min.css"
    />
  </header>
  <body>
    <div class="hello" :style="{ color: textColor }">
      <p>
        It all started about 6 months ago when I reached out to recent BU Men’s
        Rowing alum, Will Aftring. I was curious to learn more about possible
        career paths with a Computer Science degree and since Will works at
        Microsoft, I figured he would know a thing or two about that. He was
        happy to help out and offered to set me up with Matt Palmer (a Wisconsin
        University engineering student and rower who just like myself was
        looking to learn more about the world of coding) for us to work on a
        project together under supervision of himself and Riley Overfield -
        another BU Men’s Rowing alum who works at Human Interest. We set up
        weekly meetings, to discuss the project where Matt and I would share
        what we had been working on that week while also setting goals for the
        coming week. Will and Riley would then share some of the experiences and
        skills they had developed while working as programmers. This included
        information on Web Development and Computer networks - two things I had
        never worked with before, along with general work experiences and
        examples of programs they had both written.
      </p>
      <h3>First Project:</h3>
      <p>
        For a first project, Matt and I started brainstorming random ideas,
        which Will and Riley helped determine if made sense to work with. We
        came up with the idea, that we wanted to create a web app to compare
        flight prices. The app was to be written using Vue for JavaScript. The
        first step was to define what we wanted our app to do. We wanted to be
        able to find the cheapest flight and then give a score to let the user
        know how good that price was relative to other similar flights around
        the same time period. The goal was also to implement a function to
        suggest alternative forms of transportation for parts of the trip if a
        direct flight was super expensive. The second step was to set up
        wireframes, so we could see what we wanted everything to look like. The
        third step was to write the app itself. This however, is where we got
        stuck. We got all the basic functionality set up and had a landing page
        with input fields relevant for the flight search. All fields had input
        validation and auto-completion. But we unfortunately never made it
        further than that, as every single flight finder API we could find was
        blocked by a pay wall. Since we were only working on it for the sake of
        learning, we decided to scrap the project and create our own websites
        while coming up with ideas for a new project.
      </p>
      <h3>What I learned:</h3>
      <p>
        Although the final project wasn’t a massive success, I still feel like I
        picked up a lot of valuable skills on the way. Very fundamentally, I
        picked up skills in working HTML, CSS and Vue - neither of which I had
        ever worked with before. This was also the first time I ever worked on a
        bigger group coding project, so it was interesting to experience the
        dynamics of it (planning, setting goals, evaluating, etc..). I quickly
        learned that GitHub is your best friend for bigger projects. I also
        learned to check that all the relevant information needed for the
        project is easily available and not blocked by paywalls.
      </p>
      <br>
      <p>
        Having learned from the mistakes of the previous project, I now feel
        confident and excited to start working on the next.
      </p>
    </div>
  </body>
</template>

<script>
export default {
  data() {
    return {
      textColor: "grey",
    };
  },
};
</script>

<style scoped>
body {
  overflow-x: hidden;
  margin-left: 100px;
  margin-right: 100px;
  background-color: white;
}
</style>