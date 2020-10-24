<template>
<div>
<v-sheet class="align-center" color="blue lighten-5" height="150" style="text-align: center;">
<h1 class="page-title display-1" id="services-top">Recent Projects</h1>
</v-sheet>
<div style="background: #E3F2FD; width: 100%; height: 50px;padding-bottom: 0px!important;margin-bottom:0px!important;">
 <!--Waves Container-->
        <svg class="waves" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" viewBox="0 24 150 28" preserveAspectRatio="none" shape-rendering="auto">
            <defs>
                <path id="gentle-wave" d="M-160 44c30 0 58-18 88-18s 58 18 88 18 58-18 88-18 58 18 88 18 v44h-352z" />
            </defs>
            <g class="parallax">
                <use xlink:href="#gentle-wave" x="48" y="0" fill="rgba(255,255,255,1.0" />
                <use xlink:href="#gentle-wave" x="48" y="3" fill="rgba(255,255,255,1.0)" />
                <use xlink:href="#gentle-wave" x="48" y="5" fill="rgba(255,255,255,0.8)" />
                <use xlink:href="#gentle-wave" x="48" y="7" fill="rgba(255,255,255,1.0)" />
            </g>
        </svg>
    <!--Waves end-->
</div>
<v-sheet
            tile="tile"
            :elevation="0"
            class="no-round d-flex pa-2 content"
            id="bottom-content"
            width="100%"
            color="white"
          >

          
          <v-container>
          <v-row > 
          <v-col class="justify-center text-center align-center" style="margin-top: 50px;">
          <v-card class="pa-3 card content xs11 align-center text-center" flat color="white">
          <h2 class="display-1">DFW Dev</h2>
          <v-btn
          rounded
          depressed
          x-small
          color="blue lighten-1"
          class="services-btn"
          >
          Custom Software Development
          </v-btn>,
          <v-btn
          rounded
          depressed
          x-small
          color="blue lighten-1"
          class="services-btn"
          >
          Web Development
          </v-btn>,
          <v-btn
          rounded
          depressed
          x-small
          color="blue lighten-1"
          class="services-btn"
          >
          Graphic Design
          </v-btn>
          <br/>
          <p>
          This website was built by us. We didn't just install a WordPress theme and call it a day, it was created with Vue and Vuetify 
          on the frontend and a PHP Slim Backend providing RESTful services. Simply put, this website is a fullstack application and the
          frontend code is available for you to see here at <a href="https://github.com/dfw-dev" target="_blank"><v-icon small color="blue">fab fa-github</v-icon> github</a>
          </p>
          </v-card>
          </v-col>
          <v-col align="center" justify="center" class="pt-10">
          <v-responsive>
          <img class="rounded project-screenshot" 
            src="../assets/img/screenshots/dfwdev.jpg"
            :elevation="1"
          />
          </v-responsive>
          </v-col> 
          </v-row>

          <!-- start lines //-->
          <v-container fluid >
          <div class="lines-wrapper">
          <v-row> 
          <v-col class="divider-col pb-0" >
          <div class="lines-top"></div>
          </v-col>
          </v-row >
          <v-row > 
          <v-col class="pt-0 pb-0">
          <div class="lines-bottom"></div>
          </v-col>
          </v-row>
          </div>
          </v-container>
          <!-- end lines //-->

          <v-row >
          <v-col align="center" class="project-screenshot-wrap">
          <v-responsive>
          <a href="http://starkratings.com/features" target="_blank">
          <img class="rounded project-screenshot" 
            src="../assets/img/screenshots/stark.jpg"
            :elevation="1"
          />
          </a>
          </v-responsive>
          </v-col>  
          <v-col class="justify-center text-center align-center" style="margin-top: 50px;">
          <v-card class="pa-3 card content xs11 align-center text-center" flat color="white">
          <h2 class="display-1">Stark Ratings</h2>
          <v-btn
          rounded
          depressed
          x-small
          color="blue lighten-1"
          class="services-btn"
          >
          Custom WordPress Plugin
          </v-btn>,
          <v-btn
          rounded
          depressed
          x-small
          color="blue lighten-1"
          class="services-btn"
          >
          Backend Development
          </v-btn>
          <p>
          We assisted a local agency in developing a custom backend for a Dallas, Texas based startup. This project
          was custom WordPress plugin development that allows Stark Ratings to add and edit mutual funds ratings on
          their platform. 
          </p>
          </v-card>
          </v-col>
          </v-row>

          <!-- start lines //-->
          <v-container fluid>
          <div class="lines-wrapper">
          <v-row > 
          <v-col class="divider-col pt-0 pb-0">
          <div class="lines-top-mirror"></div>
          </v-col>
          </v-row >
          <v-row > 
          <v-col class="pt-0 pb-0">
          <div class="lines-bottom-mirror"></div>
          </v-col>
          </v-row>
          </div>
          </v-container>
          <!-- end lines //-->

          <v-row >
          <v-col class="justify-center text-center align-center" style="margin-top: 50px;">
          <v-card class="pa-3 card content xs11 align-center text-center" flat color="white">
          <h2 class="display-1">Design</h2>
          <br/>
          <p>
          We also offer graphic design services. Our graphic services include 
          logo, web, and UI design.  
          </p>
          </v-card>
          </v-col>
          <v-col align="center" >
          <v-responsive>
          <img class="rounded" 
            src="../assets/img/screenshots/logos.png"
            :elevation="1"
            height="300"
          />
          </v-responsive>
          </v-col>  
          </v-row>
          
          

          </v-container>
    </v-sheet>
          </div>
</template>
<script>
export default {
    layout: 'default',
    scrollToTop: true,
    head(){
    return {
      title: 'Projects',
      meta: [
        { hid: 'description', name: 'description', content: 'We have the ability to handle any web development project. Some of our recent web projects are on this page.'}

      ]
    }
  },
}

</script>
<style scoped>
.page-title{
    color: #0D47A1;
    position: relative;
    top: 100px;
}
.content{
    color: #000!important;
}
.content h2{
    color: #0D47A1;
}
.content a{
    text-decoration: none;
}
.lines-wrapper{
  padding-left: 20%;
}
.lines-top{
    width: 60%;
    height: 50px;
    border-left: 3px dashed #76FF03;
    border-bottom: 3px dashed #76FF03;
}
.lines-bottom{
    width: 60%;
    height: 50px;
    border-right: 3px dashed #76FF03;
}
/*reversed */
.lines-top-mirror{
    width: 60%;
    height: 50px;
    border-right: 3px dashed #76FF03;
    border-bottom: 3px dashed #76FF03;
}
.lines-bottom-mirror{
    width: 60%;
    height: 50px;
    border-left: 3px dashed #76FF03;
}
.project-screenshot-wrap a{
  text-decoration: none;
}
.project-screenshot{
  border: 2px solid #37474F;
}
.services-btn{
  cursor: default;
  margin: 5px 0 5px 0;
}
.waves {
  position: relative;
  width: 100%;
  height: 15vh;
  /*Fix for safari gap*/
  min-height: 100px;
  max-height: 150px;
}
/* Animation */
.parallax>use {
  animation: move-forever 25s cubic-bezier(.55, .5, .45, .5) infinite;
}
.parallax>use:nth-child(1) {
  animation-delay: -1s;
  animation-duration: 17s;
}
.parallax>use:nth-child(2) {
  animation-delay: -3s;
  animation-duration: 20s;
}
.parallax>use:nth-child(3) {
  animation-delay: -4s;
  animation-duration: 33s;
}
.parallax>use:nth-child(4) {
  animation-delay: -5s;
  animation-duration: 40s;
}
@keyframes move-forever {
  0% {
    transform: translate3d(-90px, 0, 0);
  }
  100% {
    transform: translate3d(85px, 0, 0);
  }
}
/*Shrinking for mobile*/
@media (max-width: 768px) {
  .waves {
    height: 40px;
    min-height: 40px;
    position: relative;
    top: 10px;
  }
}
</style>