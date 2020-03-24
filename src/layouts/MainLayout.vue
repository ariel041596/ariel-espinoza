
<template>
  <q-layout view="hHh LpR fFf " class="bg-accent text-white">
    <q-header bordered class="bg-accent text-white">
      <div class="row">
        <q-toolbar class="q-py-lg">
          <q-space></q-space>
          <div class="q-pl-sm">
            <q-toolbar-title class="title">
              <span class="cursor-pointer font">Ariel Espinoza</span>
            </q-toolbar-title>
          </div>
          <q-tabs
            indicator-color="transparent"
            active-color="white"
            dense
            align="left"
            class="forWeb q-ml-lg"
            v-model="tab"
          >
            <q-btn color="warning" type="a" href="#projects" flat label="Projects"></q-btn>
            <q-btn color="warning" type="a" href="#experience" flat label="Experience"></q-btn>
            <q-btn color="warning" type="a" href="#tech-stack" flat label="Technology Stack"></q-btn>
          </q-tabs>

          <q-space></q-space>
          <div class="row text-grey-6">
            <q-btn class="col facebook" icon="fab fa-facebook" flat round @click="viewFacebook"></q-btn>
            <q-btn class="col github" icon="fab fa-github" flat round @click="viewGithub"></q-btn>
            <q-btn class="col twitter" icon="fab fa-twitter" flat round @click="viewTwitter"></q-btn>
          </div>
          <q-space></q-space>
        </q-toolbar>
      </div>
      <q-tabs
        class="forMobile q-pb-sm q-mx-sm"
        indicator-color="transparent"
        active-color="white"
        dense
        align="left"
      >
        <q-btn color="warning" type="a" href="#projects" flat label="Projects"></q-btn>
        <q-btn color="warning" type="a" href="#experience" flat label="Experience"></q-btn>
        <q-btn color="warning" type="a" href="#tech-stack" flat label="Technology Stack"></q-btn>
      </q-tabs>
    </q-header>

    <q-page-container>
      <!-- <router-view /> -->
      <a name="about"></a>
      <div>
        <about></about>
      </div>
      <a name="projects"></a>
      <div>
        <projects></projects>
      </div>
      <a name="experience"></a>
      <div>
        <timeline></timeline>
      </div>
      <a name="tech-stack"></a>
      <div>
        <technology-stack></technology-stack>
      </div>
      <div></div>
      <q-page-scroller position="bottom-right" :scroll-offset="150" :offset="[18, 18]">
        <q-btn fab icon="keyboard_arrow_up" color="warning" />
      </q-page-scroller>
    </q-page-container>
  </q-layout>
</template>

<script>
import { openURL } from "quasar";
export default {
  data() {
    return {
      left: false,
      right: false,
      tab: "projects"
    };
  },
  methods: {
    viewFacebook() {
      openURL("https://www.facebook.com/chocokises");
    },
    viewGithub() {
      openURL("https://github.com/ariel041596");
    },
    viewTwitter() {
      openURL("https://twitter.com/chocokises17");
    }
  },
  components: {
    // about: require("pages/PageAbout").default,
    about: require("components/About/About").default,
    projects: require("components/Projects/MyProjects").default,
    timeline: require("components/Timeline/Timeline").default,
    "technology-stack": require("components/Technology/TechnologyStack").default
  }
};
</script>

<style lang="scss" scoped>
.facebook:hover {
  color: #157dc3;
}
.github:hover {
  color: #101010;
}
.twitter:hover {
  color: #1da1f1;
}
.font {
  font-family: monospace;
}
.title {
  font-weight: 700;
  font-size: 30px;
}
@media screen and (min-width: 767px) {
  .forMobile {
    display: none;
  }
}
@media screen and (max-width: 768px) {
  .forWeb {
    display: none;
  }
  .title {
    font-weight: 700;
    font-size: 25px;
  }
}
</style>