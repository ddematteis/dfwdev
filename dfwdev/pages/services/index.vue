<template>
<div >
<v-sheet class="half-bg" >   
<v-container>
    <v-row class="mt-15">
    <v-col class="mt-15" >
    <h1 class="page-title display-2" id="top">What We Do</h1>
    </v-col>
    </v-row>
        <!-- row //-->
          <v-row class="mx-auto">  
          <!-- col 1 //-->   
          <v-col cols="12" md="10" lg="6" xl="4">
          <v-card to="services/web-development" max-width="420" elevation="0">
          <v-responsive>
          <img  
            src="../../assets/img/screenshots/smallbiz-website1.jpeg"
            :elevation="1"
            contain
          />
          </v-responsive>
          <h2 class="service-title display-1 mt-2">Web Development</h2>
          <v-divider></v-divider>
          <b class="service-subtitle subtitle-1">We offer a variety of web development services</b>
          </v-card>

          <v-card to="services/graphic-design" class="mt-10 hidden-md-and-up" max-width="420" elevation="0">  
          <v-responsive>
          <img 
            src="../../assets/img/screenshots/presentations.jpeg"
            :elevation="1"
            contain
          />
          </v-responsive>
          <h2 class="service-title display-1 mt-2">Graphic Design</h2>
          <v-divider></v-divider>
          <b class="service-subtitle subtitle-1">Our graphic designers are skilled in web design, logos, presentations, and more.</b>
          </v-card>

          <v-card to="services/web-development/web-applications/stark-ratings" max-width="420" elevation="0" class="mt-10 mb-10">
          <v-responsive>
          <img  
            src="../../assets/img/screenshots/sr-dash.jpeg"
            :elevation="1"
            contain
          />
          </v-responsive>
          <h2 class="service-title display-1 mt-2">WordPress</h2>
          <v-divider></v-divider>
          <b class="service-subtitle subtitle-1">If you currently have a WordPress site or would like one set up, we can provide
            WordPress site migration, WordPress installation, WordPress plugin development, and WordPress theme customization services.
          </b>
          </v-card>

          <v-card to="services/agency-overflow" max-width="420" elevation="0" class="mt-10 mb-10 hidden-lg-and-up">
          <v-responsive>
          <img  
            src="../../assets/img/overflow.jpeg"
            :elevation="1"
            contain
          />
          </v-responsive>
          <h2 class="service-title display-1 mt-2">Agency Overflow</h2>
          <v-divider></v-divider>
          <b class="service-subtitle subtitle-1">We provide reliable white-label agency overflow services for development and design
            agencies.
          </b>
          </v-card>

          </v-col>
          <!-- end col 1 //-->

          <!-- col 2 //--> 
          <v-col cols="12" md="10" lg="6" xl="4">
          <v-card to="services/graphic-design" class="mt-10 hidden-sm-and-down" max-width="420" elevation="0">  
          <v-responsive>
          <img 
            src="../../assets/img/screenshots/presentations.jpeg"
            :elevation="1"
            contain
          />
          </v-responsive>
          <h2 class="service-title display-1 mt-2">Graphic Design</h2>
          <v-divider></v-divider>
          <b class="service-subtitle subtitle-1">Our graphic designers are skilled in web design, logos, presentations, and more.</b>
          </v-card>
          
          </v-col>
          <!-- end col 2//-->
          
          <!-- col 3 //--> 
          <v-col cols="12" md="10" lg="4" xl="4" class="hidden-lg-and-down">
          <v-card to="services/agency-overflow" max-width="420" elevation="0">  
          <v-responsive>
          <img 
            src="../../assets/img/overflow.jpeg"
            :elevation="1"
            contain
          />
          </v-responsive>
          <h2 class="service-title display-1 mt-2">Agency Overflow</h2>
          <v-divider></v-divider>
          <b class="service-subtitle subtitle-1">We provide reliable white-label agency overflow services for development and design
            agencies.
          </b>
          </v-card>
          
          </v-col>
          <!-- end col 3//-->

          </v-row>
        <!-- end row//-->
          
    

  </v-container>
</v-sheet> 
</div>
</template>

<script>

export default {
  layout: 'default',
  head(){
    return {
      title: 'Expert Web and Software Developers in DFW Texas',
      meta: [
        { hid: 'description', name: 'description', content: 'Based in DFW, we can build anything from small business websites to custom software.'}

      ]
    }
  },
  
  components: {
  },

  data: () => (
    {
    contentStock: require('~/assets/img/jumboStock.svg'),
    name: "",
    result: " "
  }),

  
};
</script>

<style>
.half-bg{
    /*background-color: linear-gradient( #1565C0, #01579B);*/
    height:100%!important;
    background:linear-gradient(0deg, rgba(26, 35, 126, 0.8), rgba(26, 35, 126, 0.8)), url(../../assets/img/city-stock.jpg);
    background-size: cover;
    animation: gradient 5s ease infinite;
    background-size: 100% 450px;
    background-repeat: no-repeat;
}
.page-title{
    color: #FFF;

}
.blue-block{
  color: #fff!important;
}
.blue-block a{
  color: #76FF03!important;
}
.bottom-contact{
  color: #fff!important;
}
.bottom-contact b{
  color: #76FF03;
}
.bottom-contact-btn{
  color: #fff!important;
}
.bottom-contact-btn:hover{
  color: #E1F5FE!important;
}
.content{
    color: #000!important;
}
.lines-wrapper{
  padding-left: 20%;
}
.lines-top{
    width: 60%;
    height: 50px;
    border-left: 3px dashed #03A9F4;
    border-bottom: 3px dashed #03A9F4;
}
.lines-bottom{
    width: 60%;
    height: 50px;
    border-right: 3px dashed #03A9F4;
}
/*reversed */
.lines-top-mirror{
    width: 60%;
    height: 50px;
    border-right: 3px dashed #03A9F4;
    border-bottom: 3px dashed #03A9F4;
}
.lines-bottom-mirror{
    width: 60%;
    height: 50px;
    border-left: 3px dashed #03A9F4;
}
.waves {
  position: relative;
  width: 100%;
  height: 15vh;
  margin-bottom: 0px;
  /*Fix for safari gap*/
  min-height: 100px;
  max-height: 150px;
}
/* Animation */
.parallax>use {
  animation: move-forever 25s cubic-bezier(.55, .5, .45, .5) infinite;
}
.parallax>use:nth-child(1) {
  animation-delay: -2s;
  animation-duration: 7s;
}
.parallax>use:nth-child(2) {
  animation-delay: -3s;
  animation-duration: 10s;
}
.parallax>use:nth-child(3) {
  animation-delay: -4s;
  animation-duration: 13s;
}
.parallax>use:nth-child(4) {
  animation-delay: -5s;
  animation-duration: 20s;
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
  }
  .half-bg{
        height: 500px;
    }
}
.service-subtitle{
  color: #546E7A;
}
.service-title{
  color: #37474F;
}
</style>
