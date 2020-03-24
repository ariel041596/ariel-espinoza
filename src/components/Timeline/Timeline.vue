<template>
  <q-page class="q-pa-md">
    <div class="text-center">
      <q-timeline :layout="layout" color="secondary">
        <h4 class="text-warning text-center q-pt-xl font">Works and Experience</h4>
        <q-timeline-entry
          title="Computer Operator III"
          subtitle="January 1, 2019 - March 30, 2020"
          side="left"
          color="warning"
          icon="check"
        >
          <div class>
            Works in
            <strong
              class="text-secondary"
            >Department of Information and Communciations Technology (DICT)</strong> under Asset Management Section and handle the database.
          </div>
        </q-timeline-entry>
        <q-timeline-entry
          title="Computer Operator II"
          subtitle="May 18, 2015 – December 30, 2018"
          side="right"
        >
          <div>
            Works in
            <strong
              class="text-secondary"
            >Department of Information and Communciations Technology (DICT)</strong> under Asset Management Section and handle the database.
          </div>
        </q-timeline-entry>

        <h4 class="text-warning text-center font">Trainings and Seminars Attended</h4>

        <q-timeline-entry
          color="negative"
          icon="fab fa-angular"
          title="Progressive Web Apps with Angular and Typescript"
          subtitle="September 1, 8, 15, 2019"
          side="left"
        >
          <div>
            A three (3) days training for web development using Angular 7 held by
            <strong
              class="text-secondary"
            >Ground Gurus</strong>
          </div>
        </q-timeline-entry>
        <q-timeline-entry
          color="secondary"
          icon="fab fa-vuejs"
          title="Full Stack Web and Mobile Development Training"
          subtitle="August 18, 24, 25, 31, 2019"
          side="right"
        >
          <div>
            A four (4) days training for web development using Vuejs and Quasar for front-end and Firebase, MongoDB, Express, NodeJs in the backend
            <strong
              class="text-secondary"
            >Code Stack</strong>
          </div>
        </q-timeline-entry>
        <q-timeline-entry
          color="secondary"
          icon="fab fa-vuejs"
          title="Full Stack Web Development using Progressive UI Framework and NodeJS"
          subtitle="April 27-28, 2019"
          side="left"
        >
          <div>
            A four (4) days training for web development using Vuejs and Quasar for front-end and FeathersJS, Express, NodeJs in the backend
            <strong
              class="text-secondary"
            >Web and Mobile PH</strong>
          </div>
        </q-timeline-entry>
        <q-timeline-entry
          title="Training Course in Auditing Quality Management System"
          subtitle="May 28-29, 2019"
          side="right"
        >
          <div>A two (2) days training for establishing a quality policy based on the requirements of ISO 9001:2015</div>
        </q-timeline-entry>
        <q-timeline-entry
          title="Workshop on Process Streamlining"
          subtitle="May 6-7, 2019"
          side="left"
        >
          <div>A two (2) days workshop for streamlining of the current process of the office based on the requirements of ISO 9001:2015</div>
        </q-timeline-entry>
        <q-timeline-entry
          title="Philippine eGovernment Information and Business Process Interoperability Workshop"
          subtitle="November 12-16, 2018"
          side="right"
        >
          <div>A five (5) days training together with the other government agencies representatives for establishing a one process in every departments.</div>
        </q-timeline-entry>
      </q-timeline>
    </div>
  </q-page>
</template>

<script>
export default {
  computed: {
    layout() {
      return this.$q.screen.lt.sm
        ? "dense"
        : this.$q.screen.lt.md
        ? "comfortable"
        : "loose";
    }
  }
};
</script>

<style>
</style>