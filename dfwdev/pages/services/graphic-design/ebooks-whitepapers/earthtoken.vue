<template>
<div>
<v-sheet class="align-center half-bg" >
<v-container fill-height>
    
    <v-row>
    <v-col class="pl-0 pt-15">
    <h1 class="page-title display-2 mt-10" id="top">eBook &amp; Whitepaper Design</h1>
    </v-col>
    <v-col cols="12"  class="pl-0">
    <v-breadcrumbs
      :items="items"
      large
      class="breadcrumbs"
    ></v-breadcrumbs>
    </v-col>
    </v-row>
        <!-- row //-->
          <v-row >
          <!-- col 1 //-->   
          <v-col cols="12" md="10" lg="4" xl="5" class="mt-10 hidden-sm-and-down">
          
          <v-card class="pa-10" max-width="420" elevation="0">
          <h2 class="service-title subtitle-3 mt-2">Earth Token</h2>
          <v-divider></v-divider>
          <p class="pt-5 service-subtitle subtitle-1">
            We design attractive and informative eBooks and Whitepapers. 
          </p>
          </v-card>

          <v-card color="blue darken-4 blue-block" class="mt-10 pa-10" max-width="420" elevation="0">
          <b class="overline">We can also help you with digital marketing, content writing/management, web hosting, domains, and more. If there is a service
            you need that you don't see listed here <a href="/contact">reach out</a> and we will make it happen. 
          </b>
          </v-card>

          </v-col>
          <!-- end col 1 //-->

          <!-- col 2 //--> 
          <v-col cols="12" md="10" lg="7" xl="7">
          <v-card class="mt-10" max-width="820" >  
          <v-responsive>
          <v-img :src="require('../../../../assets/img/screenshots/earth-token/1.jpg')" cover />
          </v-responsive>
          </v-card>

          <v-card class="mt-10" max-width="820" >  
          <v-responsive>
          <v-img :src="require('../../../../assets/img/screenshots/earth-token/2.gif')" cover  />
          </v-responsive>
          </v-card>

          </v-col>
          <!-- end col 2//-->
          
          <!-- col 3 mobile //-->
          <v-col cols="12" md="10" lg="4" xl="5" class="hidden-md-and-up">
          
          <v-card class="pa-10" max-width="420" elevation="0">
          <h2 class="service-title subtitle-3 mt-2">Earth Token</h2>
          <v-divider></v-divider>
          <p class="pt-5 service-subtitle subtitle-1">
            We design attractive and informative eBooks and Whitepapers. 
          </p>
          </v-card>

          <v-card color="blue darken-4 blue-block" class="mt-10 pa-10" max-width="420" elevation="0">
          <b class="overline">We can also help you with digital marketing, content writing/management, web hosting, domains, and more. If there is a service
            you need that you don't see listed here <a href="/contact">reach out</a> and we will make it happen. 
          </b>
          </v-card>

          </v-col>
          <!-- end col 3 mobile //-->
          </v-row>
        <!-- end row//-->
          
    

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
      title: 'Graphic Design - Ebooks & Whitepapers',
      meta: [
        { hid: 'description', name: 'description', content: 'We offer a wide range of web development services including: Small-business websites, custom web applications, agency overflow services, and online stores.'}

      ]
    }
  },
  data: () => ({
      items: [
        {
          text: 'Services',
          disabled: false,
          href: '/services',
        },
        {
          text: 'Graphic Design',
          disabled: false,
          href: '/services/graphic-design',
        },
        {
          text: 'eBooks & Whitepapers',
          disabled: false,
          href: '/services/graphic-design/ebooks-whitepapers',
        },
        {
          text: 'Earth Token',
          disabled: true,
          href: '/services/graphic-design/ebooks-whitepapers/earthtoken',
        },
      ],
    }),
}

</script>
<style>
.breadcrumbs{
   padding: 0px;
   margin-left: 0px;  
}
.breadcrumbs a{
    color: #00B0FF;
}
.breadcrumbs a:hover{
    color: #fff;
}
.v-breadcrumbs{
    padding-left: 5px!important;
    
}
.v-breadcrumbs__item--disabled{
    color: #B0BEC5!important;
}
.v-breadcrumbs__divider{
    color: #00B0FF!important;
}
.half-bg{
    /*background-color: linear-gradient( #1565C0, #01579B);*/
    min-height:100%;
    background:linear-gradient(0deg, rgba(26, 35, 126, 0.8), rgba(26, 35, 126, 0.8)), url(../../../../assets/img/city-stock.jpg);
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