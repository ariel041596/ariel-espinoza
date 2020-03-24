<template>
  <q-page padding>
    <div class>
      <h4 class="text-warning text-center q-pt-xl q-mb-none font">Projects</h4>
      <div class="row q-mt-lg items-start">
        <div class="col-md-6 col-xl-4 col-lg-4 col-xs-12 col-sm-12 font">
          <q-card class="q-ma-md bg-grey-12">
            <q-carousel class="img" swipeable animated v-model="slide2" thumbnails infinite>
              <q-carousel-slide class="img" :name="1" img-src="../../assets/p360-merge.png" />
              <q-carousel-slide class="img" :name="2" img-src="../../assets/p360-billing.png" />
            </q-carousel>

            <q-card-section class="text-black">
              <div
                class="text-h6"
              >Online Project Reservation with Mobile App and SMS Notification for People 360</div>
              <div class="text-subtitle2">IT Special Project</div>
            </q-card-section>
            <q-card-section class="q-pt-none text-center">
              <q-avatar class="q-mr-md">
                <img src="../../assets/firebase-logo-name.png" />
              </q-avatar>
              <q-avatar class="q-mr-md">
                <img src="../../assets/node-logo-round.png" />
              </q-avatar>
              <q-avatar class="q-mr-md">
                <img src="../../assets/vuejs-logo-round.jpg" />
              </q-avatar>
              <q-avatar class="q-mr-md">
                <img src="../../assets/Quasar-logo.jpg" />
              </q-avatar>
            </q-card-section>
          </q-card>
        </div>
        <div class="col-md-6 col-xl-4 col-lg-4 col-xs-12 col-sm-12">
          <q-card class="q-ma-md bg-grey-12">
            <q-carousel class="img" swipeable animated v-model="slide1" thumbnails infinite>
              <q-carousel-slide class="img" :name="1" img-src="../../assets/pmis-login.png" />
              <q-carousel-slide class="img" :name="2" img-src="../../assets/pmis-dashboard.png" />
            </q-carousel>

            <q-card-section class="text-black font">
              <div
                class="text-h6"
              >Property Management System for Department of Information and Communications Technology</div>
              <div class="text-subtitle2">Software Engineering Project</div>
            </q-card-section>
            <q-card-section class="q-pt-none text-center">
              <q-avatar class="q-mr-md">
                <img src="../../assets/laravel_logo-round.png" />
              </q-avatar>
              <q-avatar class="q-mr-md">
                <img src="../../assets/mysql-logo.png" />
              </q-avatar>
              <q-avatar class="q-mr-md">
                <img src="../../assets/vuejs-logo-round.jpg" />
              </q-avatar>
            </q-card-section>
          </q-card>
        </div>
        <div class="col-md-6 col-xl-4 col-lg-4 col-xs-12 col-sm-12">
          <q-card class="q-ma-md bg-grey-12">
            <q-carousel class="img" swipeable animated v-model="slide" thumbnails infinite>
              <q-carousel-slide class="img" :name="1" img-src="../../assets/RFID-Admin.png" />
              <q-carousel-slide class="img" :name="2" img-src="../../assets/RFID-User.png" />
            </q-carousel>

            <q-card-section class="text-black">
              <div
                class="text-h6 font"
              >RFID Parking Management System for Valenzuela Gateway Parking</div>
              <div class="text-subtitle2 font">System Analysis Design Project</div>
            </q-card-section>
            <q-card-section class="q-pt-none text-center">
              <q-avatar class="q-mr-md">
                <img src="../../assets/CSharp.png" />
              </q-avatar>
              <q-avatar class="q-mr-md">
                <img src="../../assets/mysql-logo.png" />
              </q-avatar>
              <q-avatar class="q-mr-md">
                <img src="../../assets/Arduino-logo-round.jpg" />
              </q-avatar>
            </q-card-section>
          </q-card>
        </div>
      </div>
    </div>
  </q-page>
</template>

<script>
export default {
  data() {
    return {
      slide: 1,
      slide1: 1,
      slide2: 1
    };
  }
};
</script>


<style lang="scss" scoped>
.font {
  font-family: monospace;
}
.img {
  height: 250px;
}
.p360 {
  height: 100px;
}
</style>