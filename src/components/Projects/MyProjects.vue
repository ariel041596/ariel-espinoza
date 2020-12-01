<template>
  <q-page >
    <div class>
      <h4 class="text-warning text-center q-pt-xl q-mb-none font">Projects</h4>
      <div class="row q-mt-lg items-start">
       <div
          v-for="(project, index) in projectsData"
          :key="index"
          class="col-md-4 col-xl-4 col-lg-4 col-xs-12 col-sm-12 font"
        >
        
          <q-card class="q-ma-md bg-grey-12" >
            
           <q-carousel
              transition-prev="scale"
              transition-next="scale"
              swipeable
              animated
              v-model="project.slide"
              height="230px"
              infinite
              thumbnails
            >
              <q-carousel-slide
                v-for="(image, index) in project.images"
                :key="index"
                :name="index"
                :img-src="image"
              > 
              </q-carousel-slide>
            </q-carousel>
            <q-card-section class="text-black" style="height: 150px;">
              <div
                class="text-h6"
              >{{project.title}}</div>
              <div
                class="text-subtitle2">{{project.subject}}
                <q-btn
                color="primary"
                v-if="project.videoURL"
                @click="showVideo(project)"
                flat
                label="Play video"
                no-caps></q-btn></div>
            </q-card-section>
            <q-card-section class="q-pt-none text-center" >
              <q-avatar class="q-mr-md" v-for="(avatar, index) in project.logos" :key="index">
                <img  :src="avatar" />
              </q-avatar>
            </q-card-section>
          </q-card>
        </div>
      </div>
     <q-dialog v-model="videoOrpng">
       <q-card style="width: 600px; max-width: 90vw; ">
         <q-video style="height:300px;" :src="this.URL" />
      </q-card>
    </q-dialog>

    </div>
  </q-page>
</template>

<script>
// Logo
const firebaseAvatar = require("../../assets/firebase-logo-name.png")
const nodeAvatar = require("../../assets/node-logo-round.png")
const vuejsAvatar = require("../../assets/vuejs-logo-round.jpg")
const quasarAvatar = require("../../assets/Quasar-logo.jpg")
const laravelAvatar= require("../../assets/Laravel-flat.jpg")
const mySQLAvatar = require("../../assets/mysql-logo.png")
const cSharpAvatar = require("../../assets/CSharp.png")
const arduinoAvatar = require("../../assets/Arduino-logo-round.jpg")

// End Logo

// 1
const p360Merge =require("../../assets/p360-merge.png");
const p360Billing= require("../../assets/p360-billing.png")
// 1

// 2
const pmisLogin = require("../../assets/pmis-login.png")
const pmisDashboard = require("../../assets/pmis-dashboard.png")
// 2
// 3
const rfidUser = require("../../assets/RFID-User.png")
const rfidAdmin = require("../../assets/RFID-Admin.png")

const projects = [
  {
    id: 1,
    images: [p360Merge,p360Billing],
    slide: 1,
    title: "Online Project Reservation with Mobile App and SMS Notification for People 360",
    subject: "IT Special Project",
    logos: [firebaseAvatar, nodeAvatar, vuejsAvatar, quasarAvatar],
    videoURL: "https://www.youtube.com/embed/7VzUjG-DnUM"
  },
  {
    id: 2,
    images: [pmisLogin,pmisDashboard],
    slide: 1,
    title: "Property Management System for Department of Information and Communications Technology",
    subject: "Software Engineering Project",
    logos: [laravelAvatar, mySQLAvatar, vuejsAvatar]
  },
  {
    id: 3,
    images: [rfidUser,rfidAdmin],
    slide: 1,
    title: "RFID Parking Management System for Valenzuela Gateway Parking",
    subject: "System Analysis Design Project",
    logos: [cSharpAvatar, mySQLAvatar, arduinoAvatar]
  }
]
export default {
  data() {
    return {
      videoOrpng: false,
      slide: 1,
      slide1: 1,
      slide2: 1,
      projectsData: projects,
      URL: null
    }
  },
  methods:{
    showVideo(project){
      this.videoOrpng = true
      this.URL = project.videoURL
    }
  }
};
</script>


<style lang="scss" scoped>
.font {
  font-family: monospace;
}

.image-fit{

}


</style>