<template>
  <q-page >
    <about></about>
    <!-- <a name="about"></a>
      <div>
        <about></about>
      </div>
      <a name="projects"></a>
      <div>
        <projects></projects>
      </div>
       <a name="events"></a>
      <div>
        <events-attended></events-attended>
      </div>
      <a name="experience"></a>
      <div>
        <timeline></timeline>
      </div>
      <a name="tech-stack"></a>
      <div>
        <technology-stack></technology-stack>
      </div>
     
      <q-page-scroller position="bottom-right" :scroll-offset="150" :offset="[18, 18]">
        <q-btn fab icon="keyboard_arrow_up" color="warning" />
      </q-page-scroller> -->
  </q-page>
</template>

<script>
export default {
  components: {
     about: require("components/About/About").default,
    // projects: require("components/Projects/MyProjects").default,
    // timeline: require("components/Timeline/Timeline").default,
    // "technology-stack": require("components/Technology/TechnologyStack").default,
    // "events-attended": require("components/Events/Events").default,
  }
};
</script>

<style>
</style>