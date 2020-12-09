<template>
  <q-page padding>
    <div class="text-center justify-center">
      <h4 class="text-warning text-center q-pt-md q-mb-none font">Technology Stack</h4>
      <div
        class="q-mt-lg text-center text-blue-grey-3 text-h6"
      >Framework/Programming Languages that I'm Familiar</div>
      <div class="row text-center justify-center">
        <div class="col-md-2 col-xl-1 col-lg-1 col-xs-4 col-sm-3 " v-for="(logo, index) in logos" :key="index">
          <q-card class="rounded q-mt-sm q-ma-xs ">
            <q-img class="rounded " :src="logo">
              <!-- <div class="text-h6 absolute-bottom text-right">Firebase</div> -->
            </q-img>
          </q-card>
        </div>
      </div>
    </div>
  </q-page>
</template>

<script>
const firebaseLogo = require("../../assets/firebase-logo-name.png")
const nodeLogo = require("../../assets/node-logo-round.png")
const vuejsLogo = require("../../assets/vue.png")
const quasarLogo = require("../../assets/Quasar-logo.jpg")
const laravelLogo= require("../../assets/Laravel-flat.jpg")
const mySQLLogo = require("../../assets/mysql-logo.png")
const cSharpLogo = require("../../assets/CSharpLogo.png")
const arduinoLogo = require("../../assets/Arduino-logo.jpg")
const angularLogo = require("../../assets/angular-logo.png")
export default {
  data(){
    return{
      logos: [laravelLogo, nodeLogo, cSharpLogo, firebaseLogo, mySQLLogo,  vuejsLogo, angularLogo, quasarLogo,  arduinoLogo]
    }
  }
};
</script>

<style lang="scss" scoped>
.rounded {
  //   border-radius: 50px;
}
</style>