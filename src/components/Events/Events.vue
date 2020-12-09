<template>
     <div class="text-center">
      <h4 class="text-warning text-center q-pt-md q-mb-none font">Events Attended</h4>
      <div class="row q-mt-lg items-start">
       <div
          v-for="(event, index) in eventsData"
          :key="index"
          class="col-md-6 col-xl-6 col-lg-6 col-xs-12 col-sm-12 font"
        >
          <q-card class="q-ma-md bg-grey-12" >
           <q-carousel
              transition-prev="scale"
              transition-next="scale"
              swipeable
              animated
              v-model="event.slide"
              infinite
              thumbnails
            >
              <q-carousel-slide
                v-for="(image, index) in event.images"
                :key="index"
                :name="index"
                :img-src="image"
              > 
              </q-carousel-slide>
            </q-carousel>
            <q-card-section class="text-black" >
              <div
                class="text-h6"
              >{{event.title}}</div>
               <div class="text-subtitle2">{{event.project}}  <q-avatar class="q-mr-md" >
                <img class="image-fit" :src="event.avatar" />
              </q-avatar></div>
              <div>
                {{event.description}}
              </div>
            </q-card-section>
          </q-card>
        </div>
      </div>
     </div>
</template>

<script>
const impactCertificate = require("../../assets/impact-certificate.jpg")
const impactJudge = require("../../assets/impact-presentation-judge.jpg")
const impactPresentation = require("../../assets/impact-presentation.jpg")
const homeCreditCompletion = require("../../assets/home-credit-completion.jpg")

const agrostatAvatar = require("../../assets/agrostat-image.jpg")
const consultMeLogo = require("../../assets/consult-me-logo.png")
const event = [
    {
        id: 1,
        images: [ impactPresentation, impactJudge, impactCertificate],
        slide: 0,
        title: "Impact Hackathon",
        project: "Agrostat",
        avatar: agrostatAvatar,
        description: "- An agriculture app that monitors the soil health and detects the weather for the reference of farmers for crop rotation. "

    },
    {
        id: 2,
        images: [homeCreditCompletion],
        slide: 0,
        title: "Home Credit Hackathon",
        project: "ConsultMe",
        avatar: consultMeLogo,
        description: "- A platform that will connects the doctors and people to have a free medical consultations in order to prevent people from taking drugs to an inappropriate symptomps."
    }
]
export default {
data(){
    return{
        eventsData : event
    }
}
}
</script>

<style lang="scss" scoped>
.font {
  font-family: monospace;
}
.image-fit{
    object-fit: cover;
}
</style>
