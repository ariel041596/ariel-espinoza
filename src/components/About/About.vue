<template>
  <div class>
    <div class="text-center">
      <q-avatar class="q-ml-md" size="150px">
        <img src="../../assets/ariel-profile.jpg" />
      </q-avatar>
      <div class="typewriter">
        <h3 class="q-mb-sm font">Hi, My name's Ariel.</h3>
        <a href="../../assets/CV.doc" download="../../assets/CV.doc">View CV</a>
        <!-- <q-btn @click="window.open('CV.doc')">Download</q-btn> -->
        <h6
          class="q-mt-sm font"
        >I'm a Full Stack Developer, currently taking BSIT at STI-College Muñoz EDSA</h6>
      </div>
      <q-space></q-space>
    </div>
  </div>
</template>

<script>
export default {
  components: {
    projects: require("components/Projects/MyProjects").default,
    timeline: require("components/Timeline/Timeline").default,
    "technology-stack": require("components/Technology/TechnologyStack").default
  }
};
</script>

<style lang="scss" scoped>
.font {
  font-family: monospace;
}

@media screen and (max-width: 768px) {
  .typewriter h3 {
    font-weight: 700;
    font-size: 28px;
  }
}

@-webkit-keyframes typing {
  from {
    width: 0;
  }
}
@-webkit-keyframes blink-caret {
  50% {
    border-color: transparent;
  }
}

h3 {
  // font: bold 300% Consolas, Monaco, monospace;
  font-family: monospace;
  border-right: 0.1em solid orange;
  width: 16.5em;
  width: 21ch;
  margin: 0 auto;
  white-space: nowrap;
  overflow: hidden;
  -webkit-animation: typing 2s steps(21, end),
    blink-caret 1s step-end infinite alternate;
}
</style>